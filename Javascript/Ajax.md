# Ajax(Asynchronous Javascript and XML)
Javascript를 이용해서 **비동기적(Asynchronous)으로 서버와 브라우저가 데이터를 교환할 수 있는 통신 방식**이다. 페이지 전체를 로드하여 렌더링할 필요가 없고 갱신이 필요한 일부만 로드하여 갱신하면 되므로 빠른 퍼포먼스와 부드러운 화면 표시 효과를 기대할 수 있다.

### 동기식 데이터 전송

<img src="https://www.nextree.co.kr/content/images/2021/01/jsseo-140509-ajax-04-1024x528.png" height="300px" width="600px">

- 서버에 데이터를 요청하고 응답이 오는 시간동안 작업을 멈추고 기다린다.

### Ajax 통신

<img src="https://www.nextree.co.kr/content/images/2021/01/jsseo-140509-ajax-05-1024x527.png" height="300px" width="600px">

- 서버에 데이터를 요청하고 응답을 기다리는 동안 자신의 다른 업무를 진행하고 응답이 오면 그 후 작업을 진행한다.

<br>

## 장점 👍

1️⃣ 웹 페이지 전체를 다시 로딩하지 않고도, 웹 페이지의 일부분을 갱신할 수 있다.  
2️⃣ 웹 페이지가 로드된 후에 서버로 데이터 요청을 보낼 수 있다.  
3️⃣ 웹 페이지가 로드된 후에 서버로부터 데이터를 받을 수 있다.  
4️⃣ 백그라운드 영역에서 서버로 데이터를 보낼 수 있다.  

<br>

## 한계 👎

1️⃣ Ajax는 클라이언트가 서버에 데이터를 요청하는 클라이언트 풀링 방식을 사용하므로, 서버 푸시 방식의 실시간 서비스는 만들 수 없다.  
2️⃣ Ajax로는 바이너리 데이터를 보내거나 받을 수 없다.  
3️⃣ Ajax 스크립트가 포함된 서버가 아닌 다른 서버로 Ajax 요청을 보낼 수 없다.  
4️⃣ 클라이언트의 PC로 Ajax 요청을 보낼 수 없다.  

<br>

## 데이터 형식

Ajax 통신에서 데이터를 전송하는 형식
- **CSV**
- **JSON**
- **XML**

<br>

## JSON
> 클라이언트와 서버 간 데이터 교환을 위한 규칙 즉 데이터 포맷

JSON은 일반 텍스트 포맷보다 효과적인 데이터 구조화가 가능하며 XML 포맷보다 가볍고 사용하기 간편하며 가독성도 좋다. JSON은 순수한 텍스트로 구성된 규칙이 있는 데이터 구조이다.

```js
{
  "name": "Jung",
  "gender": "female",
  "age": 20,
  "alive": true
}
```

<br>

## XMLHttpRequest

브라우저는 XMLHttpRequest 객체를 이용하여 Ajax 요청을 생성하고 전송한다. 서버가 브라우저의 요청에 대해 응답을 반환하면 같은 XMLHttpRequest 객체가 그 결과를 처리한다.

```js
XMLHttpRequest.open(method, url[, async])
```

|매개변수|내용|
|------|---|
|method|HTTP 메소드(GET/POST/PUT/DELETE)|
|url|요청을 보낼 url|
|async|비동기 조작 여부(default : true)|

```js
XMLHttpRequest.send   // 서버로 요청 보내기
```

<br>

## 참고
> https://poiemaweb.com/js-ajax  
> https://www.nextree.co.kr/p9521/  
> http://www.tcpschool.com/ajax/ajax_intro_basic  
