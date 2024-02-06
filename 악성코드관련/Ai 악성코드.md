**중요**
1. 악성코드 데이터에서 특징을 뽑는 것
2. 많은 양의 데이터셋을 확보하는 것

악성샘플 수집 >>> 웹 크롤링
Malshare용 오픈소스 크롤러
https://github.com/Droogy/Malget.git
apicreds.py  >>> api key 복사

malget.py -n 3  

파일 유사도 이용한 분류
ssdep, gcf (BinDiff)

해시 : 확산, 일방향

**인공지능 기술 활용을 위한 "악성코드 특징정보" (6개 카테고리의 72가지 특징정보)**  
- 메타데이터(Metadata) : 기본적인 파일정보와 PE정보  
- 정적정보(Static Info) : 개발경로 및 문자열 등 코드 내에서 확인 가능한 정보  
- 동적정보(Dynamic Info) : 레지스트리, 프로세스 등 악성코드 실행 시 동작하는 주요 행위 정보  
- 네트워크(Network) : 악성코드 실행 시 접속 시도 및 파일/메모리내 포함된 URL/IP  
- ATT&CK Matrix : 악성코드를 전략, 전술 별(TTPs) 행위를 기술단위 별로 추출한 정보  
- 기타 정보(ETC) : 악성코드 함수단위 등의 정보와 악성문서에 대한 정보

n-gram : 

string 벡터 >> string 100?  스트링의 군집을 ... 벡터화 값을 특징으로 사용. 


정규 표준분포 일때 학습이 제일 잘 됨.  

정확도를 높이자.
전처리를 잘하자.
layer 를 변경해보자.
from tensorflow.keras.callbacks import EarlyStopping 도 있다