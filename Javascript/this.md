## 일반 함수의 this와 화살표 함수의 this의 차이

✔ 자바스크립트의 내부 함수는 일반 함수, 메소드, 콜백 함수 어디에서 선언되었든지 this는 전역 객체를 가리킨다.  
✔ 일반 함수의 this는 window(전역)을 가르키며, 화살표 함수의 this는 언제나 상위 스코프의 this를 가리킨다.

<br/>

## Call, Apply, Bind 함수 : this를 바인딩하기 위한 방법

- **Call** : this를 바인딩하면서 함수를 호출한다. 두번째 인자를 apply와 다르게 하나씩 넘기는 것이다.
- **Apply** : this를 바인딩하면서 함수를 호출한다. 두번째 인자가 배열이다.
- **Bind** : 함수를 호출하는 것이 아닌 this가 바인딩 된 새로운 함수를 리턴한다.

<br/>

## use strict모드에서의 this
일반 함수에서의 this는 undefined가 바인딩 된다.

<br/>

### 참고
> https://sunnykim91.tistory.com/121
