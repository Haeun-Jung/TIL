Javascript에서 변수 선언 방식은 `var`, `let`, `const` 가 있으며, ES6에서 `let`과 `const`가 추가되었다.

<br>

# 변수 선언 방식

### var

- **변수 중복 선언이 가능**하기 때문에 예기치 못한 값을 반환할 수 있다.

```javascript
var num = 1;
console.log(num); // 1

var num = 2;
console.log(num); // 2
```

### let

- **변수 중복 선언이 불가능**하지만, **재할당이 가능**하다.

```javascript
let num = 1;
console.log(num); // 1

num = 2;
console.log(num); // 2
```

### const

- 'constant(상수)'의 의미로, **변수 중복 선언이 불가능**하고 **재할당도 불가능**하다.
- 단, **객체나 배열의 내부는 변경할 수 있다.**

```javascript
const num = 1; // 변경 불가
console.log(num); // 1
```

<br>

# 스코프(Scope)

- 유효한 참조 범위

### var(function-scoped)

- 함수 내에서 선언된 변수는 함수 내에서만 유효하며 함수 외부에서는 참조할 수 없다. 함수 내부에서 선언한 변수는 지역 변수이고 함수 외부에서 선언한 변수는 전역 변수로 취급된다.

```javascript
function func() {
  if (true) {
    var num = 1;
    console.log(num); // 1
  }
  console.log(num); // 1
}

func();
console.log(num); // ReferenceError: num is not defined
```

### let, const(block-scoped)

- 코드 블록 ({...}) 내부에서 선언된 변수는 코드 블록 내에서만 유효하며 코드 블록 외부에서 참조할 수 없다. 코드 블록 내부에서 선언한 변수는 지역 변수로 취급된다.

```javascript
function func() {
  if (true) {
    let num = 1;
    console.log(num); // 1
  }
  console.log(num); // ReferenceError: num is not defined
}

func();
console.log(num); // ReferenceError: num is not defined
```

<br>

# 호이스팅(Hoisting)

- 함수 내부에 있는 선언들을 모두 끌어올려 해당 함수 유효 범위의 최상단에 선언하는 것

### var

- 스코프에 변수를 등록(선언)하고 메모리에 변수를 위한 공간을 확보한 후, undefined로 초기화한다. 따라서 변수 선언 이전에 해당 변수에 접근하여도 undefined를 반환한다.

```javascript
console.log(num); // undefined
var num;
```

### let

- 스코프에 변수를 등록(선언)하지만 초기화는 변수 선언문에서 이루어진다. 따라서 초기화 이전에 변수에 접근하면 참조 에러(ReferenceError)가 발생한다. 스코프의 시작 지점부터 초기화 시작 지점까지의 구간을 ‘일시적 사각지대(Temporal Dead Zone; TDZ)’라고 한다.

```javascript
console.log(num); // Error: Uncaught ReferenceError: num is not defined
let num;
```

<br>

# 참고

> [let, const와 블록 레벨 스코프](https://poiemaweb.com/es6-block-scope)  
> [var, let, const 차이점](https://80000coding.oopy.io/e1721710-536f-43f2-823b-663389f5fbfa)
