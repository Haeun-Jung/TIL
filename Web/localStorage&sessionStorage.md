# Web Storage

웹 브라우저 자체에 있는 특정 저장 공간으로, HTML5에 등장하였다. 브라우저에서 제공하는 기본 API로 localStorage와 sessionStorage가 있다. 키(Key)와 값(Value)의 형태로 데이터를 저장한다. Array, Object 형태로 적용하고 싶을 시, JSON.stringify()를 사용해 문자열로 변환하여 저장한다.

<br>

# localStorage

- localStorage의 데이터는 사용자가 명시적으로 데이터를 지우지 않는 한 데이터는 영구적으로 저장된다.
- 도메인별로 생성되며, 다른 도메인의 localStorage에는 접근이 불가능하고 서로 다른 탭/창이라도 동일한 도메인이라면 동일한 localStorage를 사용한다.

<br>

# sessionStorage

- 브라우저가 열려있는 한 새로고침과 페이지 복구를 거쳐도 데이터가 남아있다.
- 페이지를 새로운 탭/창에서 열면, 세션 쿠키의 동작과는 다르게 최상위 브라우징 맥락의 값을 가진 새로운 세션을 생성한다.
- 같은 URL이라도 각각의 탭/창에 대해 새로운 sessionStorage를 생성한다.
- 탭/창을 닫으면 세션이 끝나고 sessionStorage 안의 객체를 초기화한다.
- 사용자가 많아질수록 많은 양의 서버 메모리를 필요로 한다. 이는 성능 저하로 이어질 수 있다.

<br>

## 참고

> [Window.sessionStorage](https://developer.mozilla.org/ko/docs/Web/API/Window/sessionStorage)  
> [[자바스크립트] 웹 스토리지 (localStorage, sessionStorage) 사용법](https://www.daleseo.com/js-web-storage/)  
> [[로컬 스토리지, 세션 스토리지, 쿠키]에 대해 알아보기](https://whales.tistory.com/m/56)  
> [[WEB] 웹 저장소 - 쿠키/로컬스토리지/세션스토리지](https://kangdanne.tistory.com/197?category=884096)
