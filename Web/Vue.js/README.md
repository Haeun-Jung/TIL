# Vue.js

![Vue.js](https://media.vlpt.us/images/taese0ng/post/82c7a9ee-7d30-44eb-be74-6814dd66b64c/logo-vuejs-min.png)

**컴포넌트 기반의 SPA를 구축할 수 있게 해주는 웹 프론트엔드 프레임워크**이다. MVVM(Model-View-ViewModel) 패턴을 따르며, 애플리케이션 로직과 UI 분리를 위해 설계되었다. Angular의 장점인 양방향 데이터 바인딩과 React의 장점인 가상돔 기반 렌더링 특징을 가지고 있다.

<br>

### 컴포넌트(Component)

- 웹을 구성하는 로고, 메뉴바, 버튼, 모달창 등 웹 페이지 내의 다양한 UI 요소
- 재사용 가능하도록 구조화한 것

### SPA(Single Page Application)

- 단일 페이지 애플리케이션
- 하나의 페이지 안에서 필요한 영역 부분만 로딩되는 형태
- 빠른 페이지 변환
- 적은 트래픽 양

### MVVM(Model-View-ViewModel)

- Model : 순수 자바스크립트 객체
- View : 웹페이지의 DOM
- ViewModel : Vue의 역할, View와 Model을 연결하고 보여줄 정보를 제어

![MVVM](https://012.vuejs.org/images/mvvm.png)

<br>

### 양방향 바인딩

- 화면에 표시되는 값과 프레임워크의 모델 데이터 값이 동기화되어 한쪽이 변경되면 다른 한쪽도 같이 변경되는 것

### 단방향 바인딩

- 상위 컴포넌트에서 하위 컴포넌트로 데이터가 전달되는 방식

<br>

# 참고

> [Vue.js 입문 공부(1) /view정의, 장점, 예제 등](https://mkil.tistory.com/435)  
> [Vue.js 개념 총정리(1)\_특징,장단점,컴포넌트,라이프사이클](https://mkil.tistory.com/515?category=734440)  
> [한시간만에 끝내는 Vue.js 입문](https://youtu.be/sqH0u8wN4Rs)
