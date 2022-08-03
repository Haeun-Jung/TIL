### [📌 함께하면 좋은 글](https://nykim.work/71)

<br/>

## 일반 함수의 this와 화살표 함수의 this의 차이

✔ 자바스크립트의 내부 함수는 일반 함수, 메소드, 콜백 함수 어디에서 선언되었든지 this는 전역 객체를 가리킨다.  
✔ 일반 함수의 this는 window(전역)을 가르키며, 화살표 함수의 this는 언제나 상위 스코프의 this를 가리킨다.

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

<br/>

## this의 4가지 동작 방식

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

<br/>

## Call, Apply, Bind 함수 : this를 바인딩하기 위한 방법

- **Call** : this를 바인딩하면서 함수를 호출한다. 두번째 인자를 apply와 다르게 하나씩 넘기는 것이다.
- **Apply** : this를 바인딩하면서 함수를 호출한다. 두번째 인자가 배열이다.
- **Bind** : 함수를 호출하는 것이 아닌 this가 바인딩 된 새로운 함수를 리턴한다.

<br/>

### 참고
> [프론트엔드 개발자 면접 질문(기술면접) 정리](https://sunnykim91.tistory.com/121)  
> https://poiemaweb.com/js-this  
> https://poiemaweb.com/es6-arrow-function  
> https://velog.io/@wkahd01/JS.-this%EC%9D%98-%EB%8B%A4%EC%96%91%ED%95%9C-%EC%82%AC%EC%9A%A9%EB%B2%95
