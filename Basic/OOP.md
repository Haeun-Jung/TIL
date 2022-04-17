# OOP(Object Oriented Programming) : 객체 지향 프로그래밍

**현실 세계를 프로그래밍으로 옮겨와 현실 세계의 사물들을 객체로 보고, 그 객체로부터 개발하고자 하는 특징과 기능을 뽑아와 프로그래밍하는 기법**이다. OOP로 코드를 작성하면 재사용성과 변형 가능성을 높일 수 있다.

- **추상화** : 객체의 공통된 속성들 중 필요한 부분을 포착해서 클래스로 정의하는 설계 기법이다.
- **캡슐화** : 객체의 내용 중 숨기고 싶은 부분을 외부에서 접근할 수 없게 감출 수 있다. 이는 정보의 은닉과 보호가 가능하다.
- **상속** : 부모 클래스가 자손 클래스에게 속성을 물려주는 것으로 다형성을 확보할 수 있으며, 코드의 재사용이 가능하다.
- **다형성** : 같은 형태이지만 다른 기능을 하는 것을 의미한다. 서로 다른 클래스의 객체가 같은 메시지를 받았을 때 각자의 방식으로 동작하는 능력이다.
  - **오버라이딩(Overriding)** : 상위 클래스가 가지고 있는 메서드를 하위 클래스가 재정의해서 사용
  - **오버로딩(Overloading)** : 이름의 메서드 여러개를 가지면서 매개변수의 유형과 개수가 다르도록 하는 기술

<br>

## 객체 지향 장단점
👍 재사용성이 뛰어나고 유지보수하기 쉽다.  
👎 개발 속도, 실행 속도가 느리다.

<br>

## 객체 지향적 설계 원칙
- **SRP(Single Responsibility Principle)** : 단일 책임 원칙  
  - 클래스는 단 하나의 책임을 가져야 하며 클래스를 변경하는 이유는 단 하나의 이유이어야 한다.
- **OCP(Open-Closed Principle)** : 개방-폐쇄 원칙  
  - 확장에는 열려 있어야 하고 변경에는 닫혀 있어야 한다.
- **LSP(Liskov Substitution Principle)** : 리스코프 치환 원칙  
  - 상위 타입의 객체를 하위 타입의 객체로 치환해도 상위 타입을 사용하는 프로그램은 정상적으로 동작해야 한다.
- **ISP(Interface Segregation Principle)** : 인터페이스 분리 원칙  
  - 인터페이스는 그 인터페이스를 사용하는 클라이언트를 기준으로 분리해야 한다.
- **DIP(Dependency Inversion Principle)** : 의존 역전 원칙  
  - 고수준 모듈은 저수준 모듈의 구현에 의존해서는 안된다.

<br>

## 객체 지향 언어
- JAVA
- C++
- C#
- Python

<br>

## 참고

> https://sisparang.tistory.com/38  
> https://mangkyu.tistory.com/88  
> https://theheydaze.tistory.com/603  
> https://github.com/JaeYeopHan/Interview_Question_for_Beginner/tree/master/Development_common_sense  
> https://velog.io/@co_mong/%EB%A9%B4%EC%A0%91-%EA%B3%B5%ED%86%B5-%EC%A7%88%EB%AC%B8
