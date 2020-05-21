## 질문거리
웹 크롤링이 잘 안되는 이유?

#### :date: 2020.05.19
moveTo() 메서드를 실행할 때 uncaught DOMexception 에러<br>
local server를 사용하는 게 아니라 단순하게 c:/로 시작해서 html 파일을 열었기 때문에 생긴 문제.<br>
웹 서버를 거치지 않으면 JSP를 사용할 때 비슷한 에러가 뜰 가능성이 있다. 주의!<br>

함수 선언문과 함수 표현식 - 둘 중 어느 것이 좋다는 없다.<br>
강사님 말씀 : 그런데 요즘은 함수를 string 취급하는 함수 선언문이 많이 쓰이는 추세이다. 파이썬에서 일급함수라는 키워드를 찾아보자.<br>

웹 페이지가 처음 HTML 페이지에 적혀 있는 태그들을 읽으며 생성하는 것을 "정적으로 문서 객체를 생성한다" 라고 표현한다. <br>페이지에 적혀 있는 내용을 특별한 변화 없이 생성해 붙은 이름.<br>

html(text : string)<br>
-> 브라우저 읽음(렌더링)<br>
<pre>*렌더링 과정
html -> 객체화 -> 메모리 상주 -> DOM Tree <- javascript</pre>
개발자 도구(F12)에서 html 트리를 DOM Tree라고 함<br>

document. 사용법 익히기

이벤트 이름, 이벤트 속성, 이벤트 리스너를 찾아 볼 것
마우스
키보드
...이벤트

* onclick
* onload (html : window)
* onXXX 

JAVA의 첫걸음 읽을 부분
 - 자바 언어 소개
 - 이클립스 - 스프링 개발할 것이라 쓸 것. 인텔리제이는 Android Studio
 - Java에는 함수가 없고 메서드가 있음.
 - Ch 6,7,8 = 객체 이론. 클래스를 어떻게 만들고 활용하는가
 
 5.20 일정 : Ch 2,3,4,5



## 포스팅거리

간편한 git logout : 자격 증명 관리자 -> windows 자격 증명 -> git:https://github.com ->제거하면 로그아웃 완료


#### 2020.05.20
앞으로의 방향
Java - 문법 + 기본API
DB (MariaDB - SQL)
Java - DB API
미니프로젝트

javac(컴파일) file -encoding utf8을 추가해 줘야 한다.
컴파일이란 개발자가 작성한 소스코드를 바이너리 코드로 변환하는 과정을 말한다. (목적파일이 생성됨) 
즉, 컴퓨터가 이해할 수 있는 기계어로 변환하는 작업이다. 이러한 작업을 해주는 프로그램을 가르켜 컴파일러(Compiler)라 한다.
자바의 경우, 자바가상머신(JVM)에서 실행가능한 바이트코드 형태의 클래스파일이 생성이 된다.
public이 붙는 클래스는 하나의 소스 파일에 하나만 존재한다.


오류: 기본 클래스 Hello을(를) 찾거나 로드할 수 없습니다.
https://chans-note.tistory.com/1 CLASS PATH 끝에 ;.; 추가

#### 2020.05.21
javac file.java -encoding utf8 하면 .class 파일이 생성됨
class 파일을 자바의 exe 파일이라고 생각하면 편하다

궁금했던 점 : 왜 윈도우에서만 경로에 \ (백슬래시)를 사용할까?
[설명 링크](https://onlywis.tistory.com/26)

break문이 반복문 실행의 중지라면,
continue문은 반복문 실행의 생략을 의미

책의 코드를 따라 치다가 든 생각인데, 코드를 찍은 사진을 코드로 변환시켜 줄 수는 없을까?

@15db9742 배열을 print하면 배열의 hashcode가 출력된다.
배열의 문자열을 출력하려면 toString, deepToString 메서드를 이용해야 함

eval을 java로 구현하기에서 if문은 안되는데, 그 이유는 ifelse로 문자열을 비교하려면 다른 방식으로 해야 하기 때문!
우선 switch 문을 사용하자.