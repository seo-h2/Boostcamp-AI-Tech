## DAY 02 오늘 공부한 것
- python basic
	- 파이썬 기본: 문법, 구조 등
	- 예외, 로깅 다루는 법
	- 다양한 데이터 타입(json, xml,csv..) 다루는 방법
- AI math
	- 벡터 기초

## 기억할 것

### 파이썬 기본
1. generator
	메모리를 절약할 수 있다는 것 기억하자!

2. argument 입력 순서
	(파라미터, 키워드 파라미터, 가변인자, 키워드 가변인자)

3. asterisk  * 
	함수의 인자로 들어가면 unpacking이 발생한다.
	하나만 붙이면 시퀀스 형태에, 두개 붙이면 딕셔너리 형태에 적용된다.  

4. OOP- Visibility
	Private 변수로 선언하면 타객체에서 접근하지 못한다. 
	@property 는 private변수에 접근할 수 있도록한다. 

5. decorator 
	복잡한 클로저 함수를 간단하게 만들어준다.  
	- first-class objects: 변수나 데이터 구조에 할당 가능한 객체로 파라미터나 리턴 값으로 사용가능하다. ex) map(f, val)
	- inner function: 함수 내에 또다른 함수 가 존재
	- closures: inner function을 return 값으로 반환

6. __init__파일 만들기
	(linux) `touch__init__.p`
	3.3+부터는 없어도 패키지로 인식한다. 

7. 상대참조 호출
	`from ..sound.echo import echo_test`
	`..`은 부모 디렉토리 기준으로, sound 상위폴더의 echo 를 사용한다. 

8. 가상환경 
	`conda create -n my_project python = 3.9` 생성
	`conda deactivate` 가상환경 해제
	`conda install matplotlib` 패키지 설치
	콘다 사용하는 이유: 파이썬 코드가 아닌 코드를 설치할 때 콘다는 컴파일을 자동으로 해준다. 

### file/ exception/ log handling
1. raise <Exception Type> (예외정보)
	필요에 따라 강제로 exception발생
	
2. text 파일/ binary 파일
	- text: 인간 이해할 수 있음, 메모장으로 킬 수 있음
	- binary: 컴퓨터만 이해할 수 있음, 이진법 형식으로 저장, 메모장 해설 불가- 어플리케이션에 종속됨, 엑셀을 지원하는 파일에서만 열 수 있다. 

3. 파일 복사 shutil

    source= "s.txt"
    dest= os.path.join("abc", "sh.txt")
    shutil.copy(source, dest) 

	source파일을 dest경로에 복사
	최근에는 pathlib을 많이 사용

4. pickle
	객체는 메모리에 있다. 파이썬 인터프리터 끝나면 사라진다. 이후에도 계속 쓰고 싶을 땐 pickel 사용해 영속화 시킨다. 
	저장해야하는 모델이나 데이터가 있을 때 사용
	
	import pickle
	f= open("list.pickle", "wb")
	test=[1,2,3]
	pickle.dump(test, f)
	
5. logging
	- 로그 관리 모듈 logging
	- level: debug(개발)>info(처리 진행중)>warning(의도치 않은 정보가 들어왔을떄)>error>critical (사용자에게 보여짐)
	- configparser, argparse(프로그램 실행시 setting정보 저장)
	
### python data handling
1. vc에서 정규식
	ctrl + h 로 정규표현식 찾아볼 수 있음
	regexr.com 연습 페이지
	


## 회고
코드 작성할 때 모듈화하는 연습을 해야겠다! 
기본이 제대로 갖춰져 있어야 나중에 편하다. 오늘 배운 것들 모두 잊지말고 기억해서 많이 써먹어보자! 
