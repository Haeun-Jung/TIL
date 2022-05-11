# Promise

ES6에서 새롭게 도입한 **Promise는 자바스크립트 비동기 처리에 사용되는 객체**로, 생성자를 통해 인스턴스화한다. Promise는 성공할 때는 resolve를 호출해주면 되고, 실패할 때는 reject를 호출해주면 된다.
Promise를 사용하면 콜백 지옥(CallBack Hell)을 벗어날 수 있다. 
new 연산자와 함께 호출한 Promise의 인자로 넘겨주는 콜백함수는 호출할 때 바로 실행, 그 내부에 resolve 또는 reject 함수를 호출하는 구문이 있으면 둘 중 하나가 실행되기 전까지는 다음 then or catch 구문으로 넘어가지 않는다.

> **콜백 지옥** : 콜백 함수를 익명 함수로 전달하는 과정에서 또 다시 콜백 안에 함수 호출이 반복되어 코드의 들여쓰기 수준이 감당하기 힘들 정도로 깊어지는 현상

![Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise/promises.png)

<br/>

## Promise의 상태
- **대기(pending)**: 이행하지도, 거부하지도 않은 초기 상태
- **이행(fulfilled)**: 연산이 성공적으로 완료
- **거부(rejected)**: 연산 실패

<br/>

## 예제
```javascript
let myFirstPromise = new Promise((resolve, reject) => {
  // 비동기 작업이 성공한 경우 resolve(...)를 호출, 실패한 경우 reject(...)를 호출
  // XHR/HTML5 API
  setTimeout( function() {
    resolve("성공!")
  }, 250)
})

myFirstPromise.then((successMessage) => {
  // successMessage는 위에서 resolve(...) 호출에 제공한 값
  // 문자열이라고 가정
  console.log("와! " + successMessage)
});
```

<br/>

## 참고

> https://amyhyemi.tistory.com/m/224  
> https://espania.tistory.com/341  
> https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise
