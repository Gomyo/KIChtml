## 질문거리
웹 크롤링이 잘 안되는 이유?

#### :date: 2020.05.19
moveTo() 메서드를 실행할 때 uncaught DOMexception 에러  
local server를 사용하는 게 아니라 단순하게 c:/로 시작해서 html 파일을 열었기 때문에 생긴 문제.  
웹 서버를 거치지 않으면 JSP를 사용할 때 비슷한 에러가 뜰 가능성이 있다. 주의!  

함수 선언문과 함수 표현식 - 둘 중 어느 것이 좋다는 없다.  
강사님 말씀 : 그런데 요즘은 함수를 string 취급하는 함수 선언문이 많이 쓰이는 추세이다. 파이썬에서 일급함수라는 키워드를 찾아보자.  

웹 페이지가 처음 HTML 페이지에 적혀 있는 태그들을 읽으며 생성하는 것을 "정적으로 문서 객체를 생성한다" 라고 표현한다.  
페이지에 적혀 있는 내용을 특별한 변화 없이 생성해 붙은 이름.  

```
html(text : string)  
-> 브라우저 읽음(렌더링)  
렌더링 과정
html -> 객체화 -> 메모리 상주 -> DOM Tree <- javascript
개발자 도구(F12)에서 html 트리를 DOM Tree라고 함  
```

TODO : document 사용법 익히기

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

md emoji 클릭하면 복사되는 프로그램을 만들어 볼까?
간편한 git logout : 자격 증명 관리자 -> windows 자격 증명 -> git:https://github.com ->제거하면 로그아웃 완료
5.25 : ArrayMain01
객체지향 프로그래밍의 4대 개념 (OOP is A P.I.E) 시리즈 포스팅

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

#### 2020.05.22
클래스 별로 독립적인 파일을 만들자

Class
    변수(속성:상태) - 멤버변수(field)
    함수(기능) - (멤버)Method
    *Class - 희소한 경우로 클래스 내 클래스가 있을 수 있다

(객체/참조)변수(instance)로써 선언 - 인스턴트화 : new

참조변수의 선언
클래스 참조변수명;

참조변수의 생성
참조변수명 = new 클래스명();

초기화/사용 : .

클래스  
    메서드이름  
    메서드이름  
    *선언 가능하게 하기 - Method Overloading(중복 정의)


    인스턴스 멤버 필드
    클래스 멤버 필드

    메서드
        지역 변수
        인스턴스
        클래스
        *오버로딩(중복 정의)
            같은 이름 메서드 선언 가능
            숟가락, 포크, 젓가락 모두 먹다.
            그런데 메서드 이름을 spoonEat, forkEat, ChopEat ? -> 너무 비효율적!
            인자만 바꾸어 적용할 수 있도록 하면 편할 것이다. 이때 오버로딩이 필요함!

지역변수 초기화의 방법
    - 새 값을 부여
    - 파라미터에서 갖다 쓰기

생성자의 역할  
멤버 변수의 설정  

#### 2020.05.25

클래스
    멤버필드
        인스턴스 / 클래스
    메서드
        지역변수 / 제어문
        *인스턴스 / 클래스
        *오버로딩(중복정의)
        *main(실행메서드 -> 실행클래스)
        *constructor
            구별법
                클래스명과 동일
                리턴없음
            역할
                메모리 생성
                멤버변수 초기화
{
    블럭
    블럭 내부에 생성된 변수를 지역변수라고 함
}

**플로우차트**


**UML 다이어그램 - 프로그램의 기획**
Class diagram
    클래스의 구성 요소와 연관 관계
Sequence diagram
    프로그램의 흐름
Usecase diagram
    기능구조

툴
    StarUML
    Rational Rose
    Amateras - Eclipse Plugin


클래스의 연관

    1. Instance : 포함관계 has a
        class {className} {
            int data;
            className data;

            String data;
        }
    2. Inheritance : 상속관계. 부모의 재산 : 멤버 변수와 메서드 is a

        형식
        
        class {child,sub} extends {parent,super}   {

        }

        UML / 초기화블럭, 생성자는 상속 불가 

        오버라이딩 (ADS @Override가 여기서 나온 거였구나)

#### 2020.05.26
package가 다르다면, 굳이 import 하지 않으면 class를 가져다 쓰지 않는다.
즉, package가 다르면 class 명이 중복 되어도 된다.

지금 우리는 디렉토리를 구분하지 않고 있는데, 나는 일자에 따라 분류하고 있다.
package를 선언하지 않았지만, 알아서 선언이 되는 것인지 = 아니다. package 선언을 해야 가능

기본적으로 package를 쓰는 것이 좋은지

final
    지역변수    -상수
    멤버변수

    메서드      -오버라이드 금지
    클래스      -상속 금지

같은 package 안에 있는 class를 가지고 오더라도 import를 해야 하는가?
- ㄴㄴ

eclipse 환경설정

font - basic - font font 

Spelling unable

workspace - text file encoding을 utf-8로

**clipse**
1. 프로젝트(Java)
    패키지(X / default package)

생성자 만들 때
생성자 이름 치고 Ctrl + Space : 자동 완성

#### 2020.05.27

상속
has a : 멤버필드
is a : 상속
    extends
    overriding
        조건
    super
    super() / this()


editor : 소스를 편집
IDE : Integrated Development Environment 
    - 통합 개발자 환경
    - Code Assistance
    - Debugging
    - 자동 컴파일(바로 실행 가능)

개발 순서
    프로젝트
        패키지
            클래스

#### 2020.06.01

        변수
        상수
        *식별자 규칙
            문법
            *팀원간의 룰
            패키지명, 클래스명, 메서드명, 변수명
    연산자
        단항 : 부호 / 증감 (++ --)
        이항 : 나머지 전부
        삼항 : ? (if)
    형변환
        자동형변환
        묵시적형변환

제어
    조건에 의한 분기
        - 선택 : 중첩 if (if else / switch)
        - 필터링 : 단순조건
    조건에 의한 반복
        - 유한 루프
            for
                일반
                향상된 for ( : )
        - 무한 루프
            while
            do ~ while
    기타 : 반복문의 제어 목적. continue / break / label


- 객체중심 프로그램 언어 문법

class 

jdk 1.10부터 module이 나옴
module
    package
        package / import , package comfile method (-d ./ 옵션 기억하기)

        interface
        class
            일반클래스
            추상클래스
                멤버변수
                    인스턴스 / 클래스
                메서드
                    인스턴스 / 클래스
                    추상 메서드 (abstract class + method = addFuel() 생각하기)

                    오버로딩

                    생성자
                    메인메서드

                    가변인자 Variable Argument (파라미터를 모르겠을 때 임의의 값을 받게끔 하는 메서드)
                        Warning! 오버로딩과 같이 사용 불가
                초기화블럭
                    종류
                내부클래스
                    종류
        enum
        exception

캡슐화(은닉화)
    접근지정자
    private, default, protected, public
상속화
    인터페이스(interface) / 클래스(class)
    오버라이드
    super, super()
    Object
추상화
    Interface
    abstract class
다형성
    형변환
    오버라이드

API(라이브러리)
package 단위로 제공
    - class -> *.jar 인스톨 개념이 아니라 원하는 위치에 복사하면 끝
- Oracle 제공
    java : 기본 패키지
        java.lang 기본 패키지. import not needed
            Object
            String(Javascript)

    javax : 확장 패키지
- Third part (* 제 3의 업체에서 제공)

문자열 관련된 클래스 
String / StringBuffer / StringBuilder