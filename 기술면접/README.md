## ☑ Network

### Q. 캡슐화
송신지 호스트의 각 계층을 지날 때마다 해당 계층의 프로토콜을 처리하고 데이터에 헤더를 추가하는 것

### Q. 물리 계층
OSI 모델의 최하위 계층으로, 데이터를 전송하기 위해 시스템간의 물리적인 연결을 하고 전기 신호의 변환 및 제어하는 역할을 담당하는 계층

### Q. 네트워크 계층
OSI 모델에서 다른 네트워크와 통신하기 위한 경로 설정을 위해 라우터를 통한 라우팅을 하며 패킷 전송을 담당하는 계층

### Q. IP (Internet Protocol)
네트워크 상에서 데이터를 교환하기 위한 프로토콜

### Q. fragmentation(조각화, 단편화)
큰 IP 패킷들이 작은 MTU ( Maximum transmisson Unit )을 갖는 링크를 통하여 전송되려면 여러 개의 작은 패킷으로 쪼개어져야 하는데 이를 fragmentation라고 한다.

### Q. HTTP / HTTPS의 약속된 포트 번호
80 / 443

### Q. TCP
인터넷에 연결된 컴퓨터에서 실행되는 프로그램 간에 통신을 안정적으로 순서대로 에러없이 교환 할 수 있게 하는 프로토콜

### Q. 3-Way-HandShake
클라이언트가 서버에게 요청 패킷을 보내고, 서버가 클라이언트의 요청을 받아들이는 패킷을 보내고 클라이언트는 이를 최종적으로 수락하는 패킷을 보내는 과정

### Q. 4-Way-HandShake
세션을 종료하기 위해 수행되는 절차

### Q. HTTP 프로토콜 중 'PATCH'
리소스의 부분을 수정하는데 사용하며 의미론적으로 UPDATE와 더 가까운 HTTP 메소드

### Q. URI(Uniform Resource Identifier)
특정 리소스를 식별하는 통합 자원 식별자. 자원을 나타내는 유일한 주소

### Q. URL(Uniform Resource Locator)
흔히 웹 주소라고도 하며, 컴퓨터 네트워크 상에서 리소스가 어디 있는지 알려주기 위한 규약

<br>

## ☑ OperatingSystem

### Q. Context Switching(문맥교환)
단일 CPU를 여러 프로세스에서 공유할 수 있는 방법 중의 하나로, CPU를 점유하는 프로세스가 나가고 새로운 프로세스가 들어오는 상황

### Q. 인터럽트 발생시 동작 순서
1️⃣ 인터럽트 요청 신호 발생  
2️⃣ 현재 수행 중인 프로그램 상태 저장  
3️⃣ 어느 장치가 인터럽트를 요청했는지 탐색  
4️⃣ 인터럽트 취급 루틴 수행  
5️⃣ 보존한 프로그램 상태로 복귀  

### Q. 선점형 스케줄링
어떤 프로세스가 CPU를 할당받아 실행 중이더라도 운영체제가 CPU를 강제로 빼앗을 수 있는 스케줄링

### Q. HRN 스케줄링
서비스를 받기 위해 대기한 시간과 CPU 사용 시간을 고려하여 우선순위를 정하는 스케줄링 알고리즘

### Q. 라운드 로빈 스케줄링
프로세스가 할당받은 시간(타임 슬라이스)동안 작업하다가 완료하지 못하면 준비 큐의 맨 뒤로 가서 다음 자기 차례가 올때까지 기다리는 선점형 스케줄링 알고리즘 중 가장 단순한 것

### Q. 교착 상태
2개 이상의 프로세스가 다른 프로세스의 작업이 끝나기만을 기다리며 작업을 더 이상 진행하지 못하는 상태

### Q. 경쟁 상태
프로세스 내에서 여러 실행 흐름이 존재할 수 있게 되면서 동기화 문제가 대두되는데, 여러 스레드가 동시에 공유 자원을 접근하려는 경우 발생하는 상태

<br>

## ☑ Javascript

### Q. Arrow Function을 사용하는 이유는?
ES5에서는 함수 호출시 this가 전역 객체를 가리키는데 반해 `Arrow Function은 상위 환경의 this를 계승받는다.`
```js
function Prefixer(prefix) {
  this.prefix = prefix;
}
Prefixer.prototype.prefixArray = function (arr) {
  // this는 상위 스코프인 prefixArray 메소드 내의 this를 가리킨다.
  return arr.map(x => `${this.prefix}  ${x}`);
};
const pre = new Prefixer('Hi');
console.log(pre.prefixArray(['Lee', 'Kim']));
```

### Q. 자바스크립트에서 this는 몇가지로 추론할 수 있나요?
1️⃣ `일반 함수에서의 this` : window(전역 객체), 내부 함수(일반 함수, 메소드, 콜백함수)는 모두 전역객체 바인딩  
2️⃣ `메소드에서 this` : 메소드를 소유한 객체  
3️⃣ `생성자 함수에서 this` : 객체 속성 할당을 위해 사용  
4️⃣ `명시적 this` : 특정 객체에 바인딩이 가능(apply, bind, call)  

```js
var foo = function () {
  console.dir(this);
};
// 1. 함수 호출
foo(); // window
// window.foo();
// 2. 메소드 호출
var obj = { foo: foo };
obj.foo(); // obj
// 3. 생성자 함수 호출
var instance = new foo(); // instance
// 4. apply/call/bind 호출
var bar = { name: 'bar' };
foo.call(bar);   // bar
foo.apply(bar);  // bar
foo.bind(bar)(); // bar
```

<br>

## ☑ Web

### Q. AJAX
AJAX는 비동기적 웹 어플리케이션의 제작을 위해 이용하는 웹 개발 기법으로 주로 회원가입시 아이디 중복검사나 비밀번호 유효성 검사 등에 사용한다. 웹 페이지는 화면을 이동할 때마다 화면의 콘텐츠를 다시 가져와서 표시하는데, 웹 서비스 중에는 현재의 화면을 그대로 둔 채로 특정 영역의 데이터를 추가/삭제/변경 등의 기능을 쓸 때 AJAX를 활용한다. AJAX를 사용하면 화면 전체를 재로딩함으로써 발생하는 트래픽의 증가도 필요한 영역의 적은 데이터만 통신함으로써 트래픽을 줄이는 효과가 있다.

### Q. 웹 브라우저 검색창에서 키워드를 입력하면 결과가 나오는 과정
웹 브라우저에 검색 창에 키워드를 입력하면 웹 사이트의 검색창에 정의된 form의 method(get/post)의 방식으로 action에 기록된 서버로 검색 키워드로 전송하게 된다. 서버는 검색 키워드를 전송 받으면 검색 키워드와 관련하여 구현된 비즈니스 로직을 실행시키고, 그 결과는 HTML로 구성하여 다시 웹 브라우저로 전송한다. 웹 브라우저는 서버로부터 새로운 HTML이 오면 결과를 화면에 보여지게 한다.

### Q. 웹 브라우저 앞으로가기, 되로가기를 구현할 때에 어떤 자료구조를 사용할 것인가
스택을 사용할 것이다. 스택은 최근에 들어간 데이터를 처음 꺼낼 수 있는 형태이다. 뒤로가기는 페이지를 이동하면서 새로 보여지는 페이지의 정보를 스택에 저장하고 있다가 뒤로가기를 하고 싶을 때에는 스택의 맨 위에 있는 데이터를 꺼내서 이동하면 된다.

### Q. Virtual DOM 설명
DOM의 가벼운 복사본으로, `Virtual DOM은 DOM이 생성되기 전, 이전 상태 값과 수정사항을 비교하여 달라진 부분만 DOM에게 한 번에 전달하여 딱 한 번만 렌더링을 진행`한다.

### Q. What Happens When You Type google.com
![동작원리](https://s3-ap-northeast-2.amazonaws.com/opentutorials-user-file/module/3421/8340.jpeg)

1️⃣ 각 운영체제 hosts 파일 내용 확인    
2️⃣ hosts 파일로 IP 주소를 알아내지 못하면, DNS 서버에게 질의    
3️⃣ IP 주소를 이용하여, `google.com` 접속 및 통신

### Q. 브라우저 렌더링 과정
1️⃣ DNS로 도메인을 IP 주소로 바꿔준다.  
2️⃣ HTTP 또는 HTTPS를 이용하여 요청한다.  
3️⃣ Loading: HTTP 모듈 또는 파일 시스템으로 전달 받은 리소스 스트림을 읽는다.  
4️⃣ DOM: HTML을 파싱하여 DOM Tree를 빌드한다.  
5️⃣ CSSOM: CSS를 파싱하여 CSSOM 트리를 빌드한다.  
6️⃣ Render Tree: DOM과 CSSOM을 결합하여 렌더링 트리를 만든다.  
7️⃣ Layout: 렌더링 트리가 화면상에 어떻게 배치할 것인지를 계산한다.  
8️⃣ Paint: 화면에 표시한다.  

### Q. Vue와 React의 차이점
`Vue.js` : 프레임워크, 양방향 데이터 바인딩  
`React` : UI 라이브러리, 단방향 데이터 바인딩

### Q. Vue의 라이프사이클
1️⃣ `created` : 인스턴스의 생성  
2️⃣ `mounted` : 생성된 인스턴스를 화면에 부착  
3️⃣ `updated` : 화면에 부착된 인스턴스의 내용 갱신  
4️⃣ `destroyed` : 인스턴스가 소멸  

<br>

## ☑ ETC

### Q. 리팩토링
결과의 변경 없이 코드의 구조를 재조정하여 가독성을 높이고 유지보수를 편하게 하는 데 적용되는 방법

### Q. 이더넷, 인터넷, 인트라넷 설명
`이너뎃` : lan을 위해 개발된 네트워크 기술로 osi 모델의 물리계층에서 신호와 배선, 데이터링크계층에서 mac패킷과 프로토콜의 형식  
`인터넷` : 누구에게나 공개되어 있는 망으로 isp(internet service provider)를 사용(공인ip)  
`인트라넷` : 전용선을 사용하여 구성하는 망으로 인터넷과의 연결을 배제하는 망(사설ip)

<br>

## 참고
> https://kim-solshar.tistory.com/57   
> https://poiemaweb.com/es6-arrow-function  
> https://velog.io/@dkdlel102/%EB%A9%B4%EC%A0%91-%EC%98%88%EC%83%81-%EC%A7%88%EB%AC%B8-%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80-%EB%8F%99%EC%9E%91-%EC%9B%90%EB%A6%AC-HTTP-%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC  
> https://velog.io/@wkahd01/JS.-this%EC%9D%98-%EB%8B%A4%EC%96%91%ED%95%9C-%EC%82%AC%EC%9A%A9%EB%B2%95  
> https://poiemaweb.com/js-this  
> https://it-eldorado.tistory.com/55  
> https://blog.daum.net/g_g/12  
