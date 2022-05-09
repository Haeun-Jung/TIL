# React
> **사용자 인터페이스를 만들기 위한 Javascript 라이브러리**
![](https://images.velog.io/images/katej927/post/55cef9b8-4c8c-48a8-81fb-9275465ba5cc/react.jpg)

React에서는 인터렉션이 발생하게 되면 바로 브라우저의 DOM에 접근하여 변화를 반영하는 것이 아니라 Virtual DOM에 한 번 렌더링하고, 이를 기존의 DOM과 비교하여 **변화가 필요한 곳만 렌더링**한다.

<br/>

### 컴포넌트(Component)
- 컴포넌트 기반의 라이브러리
- 재사용 가능하도록 구조화한 것

### Props and State
- 단방향 데이터 흐름(one-way data flow) 
- 부모에서 자식, 한방향으로만 흐르며 거꾸로 부모의 데이터를 바꿔주기 위해서는 state 이용

### 가상 돔(Virtual DOM)
- DOM과 유사한 객체를 메모리에 올려놓고, 변경 사항이 생기면 Virtual DOM을 바꾸고, 실제 DOM에서는 변경 사항만 변경할 수 있게 하여 더 반응성이 빠른 웹을 구현 가능

### JSX
- JSX(JavaScript XML)는 Javascript에 XML을 추가한 확장한 문법으로, 리액트에서 element 제공

<br/>

## 장점👍
- 간편한 UI 수정이 가능하며 재사용이 용이하다.
- 다른 프레임워크나 라이브러리와 혼용하여 사용할 수 있다.
- 서버 사이드 렌더링과 클라이언트 사이드 렌더링 모두 지원한다.
- Controller, directive, template, model 처럼 분리를 하지 않고 Component 하나로 관리한다.
- 뛰어난 Garbage Collection, 메모리 관리, 성능을 가지고 있다.

 <br/>

## 단점👎

- view 외 기능은 직접 구현하거나 라이브러리를 사용하여 구현해야 한다.
- 데이터 모델링, Routing, Ajax 등의 기능을 제공하지 않는다.
- IE8 이하 버전을 지원하지 않는다. 

<br/>

## 참고
> https://ko.reactjs.org/  
> https://pp-ppi.tistory.com/41  
> https://goddaehee.tistory.com/295  
> https://edu.goorm.io/learn/lecture/16422/%EA%B0%80%EC%9E%A5-%ED%95%AB%ED%95%9C-fe-%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC-react-%EA%B0%80%EC%A7%80%EA%B3%A0-%EB%86%80%EC%95%84%EB%B3%B4%EA%B8%B0/lesson/784014/react%EC%9D%98-%ED%8A%B9%EC%A7%95-%EB%B0%8F-%EC%9E%A5%EC%A0%90
