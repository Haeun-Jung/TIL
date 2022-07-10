# 화살표 함수
- **함수를 정의할 때 `function`이라는 키워드를 사용하지 않고 `=>`로 대체**
- 흔히 사용하는 콜백 함수의 문법을 간결화
- 함수 내부 내용이 반환값(return)만 있다면 코드 블록(함수의 몸통)인 중괄호({})와 return 생략 가능
- 인자가 하나인 경우 매개변수의 괄호() 생략이 가능하지만, 인자가 없거나 여러 개인 경우 생략 불가


```javascript
// ES5
var sum = function (x, y) {
   return x + y;
};

// ES6
var sum = (x, y) => {
   return x + y;
}

sum (1, 1);
```


```javascript
var arr = [1, 2, 3];

// ES5
var pow = arr.map(function (x) {
  return x * x;
});

console.log(pow); // [ 1, 4, 9 ]

// ES6
const pow = arr.map(x => x * x);

console.log(pow); // [ 1, 4, 9 ]
```

<br>

## 화살표 함수의 this
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

<br>

## 📌 주의사항
✔ this나 super에 대한 바인딩이 없고, methods로 사용될 수 없다.  
✔ new.target 키워드가 없다.  
✔ 스코프를 지정할 때 사용하는 call, apply, bind methods를 이용할 수 없다.  
✔ 생성자(Constructor)로 사용할 수 없다.

<br>

## 참고
> https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions/Arrow_functions  
> https://github.com/WeareSoft/tech-interview/blob/master/contents/javascript.md#%ED%99%94%EC%82%B4%ED%91%9C-%ED%95%A8%EC%88%98  
> https://poiemaweb.com/es6-arrow-function
