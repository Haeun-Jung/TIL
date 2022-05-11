## async/await
✔ **목적** : 사용하는 여러 Promise의 동작을 동기스럽게 사용할 수 있게 하고, 어떠한 동작을 여러 Promise의 그룹에서 간단하게 동작하게 하는 것

async와 await는 **자바스크립트의 비동기 처리 패턴** 중 하나이다. 기존의 비동기 처리 방식인 Callback 함수와 Promise의 단점을 보완하고 개발자가 읽기 좋은 코드를 작성할 수 있게 도와준다.  
함수 선언자 앞에다가 async를 붙여주고, 비동기가 필요한 작업 앞에다가 await를 붙여서 결과를 기다린다. 다수의 비동기 처리 작업을 할 때 유용하고, **try/catch를 이용해서 에러를 핸들링 할 수 있다.**

> await 키워드는 async 함수에서만 유효하다. async 함수의 본문 외부에서 사용하면 SyntaxError가 발생한다.


<br/>

## 기본 문법
```javascript
async function 함수명() {
  await 비동기_처리_메서드_명();
}
```

<br/>

## Promise와 차이점
 - Promise는 .catch()로 에러 핸들링이 가능하다. 하지만, async/await은 에러 핸들링 기능이 따로 없기 때문에 try/catch를 활용한다.
 - Promise는 .then()을 계속 반복할 우려가 있다. 코드가 길어질수록 async/await을 사용하면 가독성이 좋아진다.

<br/>

## 참고
> https://amyhyemi.tistory.com/m/224  
> https://joshua1988.github.io/web-development/javascript/js-async-await/  
> https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/async_function
