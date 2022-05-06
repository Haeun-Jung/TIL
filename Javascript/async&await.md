## async/await
async와 await는 **자바스크립트의 비동기 처리 패턴** 중 하나이다. 기존의 비동기 처리 방식인 Callback 함수와 Promise의 단점을 보완하고 개발자가 읽기 좋은 코드를 작성할 수 있게 도와준다.  
함수 선언자 앞에다가 async를 붙여주고, 비동기가 필요한 작업 앞에다가 await를 붙여서 결과를 기다린다. 다수의 비동기 처리 작업을 할 때 유용하고, **try/catch를 이용해서 에러를 핸들링 할 수 있다.**

<br/>

## 기본 문법
```javascript
async function 함수명() {
  await 비동기_처리_메서드_명();
}
```

<br/>

## 참고
> https://amyhyemi.tistory.com/m/224  
> https://joshua1988.github.io/web-development/javascript/js-async-await/
