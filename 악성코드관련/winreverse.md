악성코드를 실행한 폴더의 모든 hwp을 대상으로 감염시킨다.
GetCurrentDirectoryA 
FindFirstFileA  : 감염시킬 첫번째 파일을 찾는다. 파일이 없으
WriteFile 로 파일을 쓰기 위해   ???

GetFileSize 로 사이즈를 읽어옴.

ReadFile로 파일의 내용을 읽어서 처음내용이 0xFFFFFFFF 면 감염된것으로 파악 > 다음 파일로 이동

파일을 한 바이트씩 읽어서 Xor 계산 : BD
eax를 카운트로 씀. ebp에 파일크기를 넣음.

SetFilePointer로 파일의 처음을 가르킴. 

첫번째 writefile 4byte 모르겠음
두번째 writefile xor 연산한 걸 파일에 씀

처음 F4C를 뺀다. 지역변수 할당을 위해



