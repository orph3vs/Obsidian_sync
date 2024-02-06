mini100

69 <- push ax 감염 후 파일 크기
0  <- push cx  ? ffff크기 만큼 읽어올려고 
164 <- 바이러스의 다음 위
083F  <- 바이러스 복사본이 있는 주소 
100 <- push si  바이러스 시작점 

메모리 직렬화 
73f:100 == 0:74f0


73f 코드 세그먼트    일종의 방
73f -> 73f0 + 100 >> 74f0

주소 비트를 확장하기 위함

REPZ      cx 레지스터가 0이 될때까지 반복 
MOVSB
DS:SI   메모리 내용을 ES:DI 가 가르키고 있는 곳으로 복사


백신
11c 검출 로직
128 치료 로직
013e  VIRUSalksdjfksdjf
014b  cx가 0이면 파일 포인터 이후는 짤라버림  

문제점1. closehandle이 없음, handle leak
문제점2. 중복감염에 대한 처리가 안되어있음 

문제점 해결 해보기.


x64 디버깅 

ultra string Refrerence