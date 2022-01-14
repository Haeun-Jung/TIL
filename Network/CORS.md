# CORS(Cross-Origin Resource Sharing)

추가 HTTP 헤더를 사용하여, 한 출처에서 실행 중인 웹 애플리케이션이 **다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여**하도록 브라우저에 알려주는 체제이다.

<br>

## SOP(Same-Origin Policy)

**같은 출처에서만 리소스를 공유할 수 있다**라는 규칙을 가진 정책이다. SOP는 XSS나 XSRF 등의 보안 취약점을 노린 공격을 방어할 수 있다.

- 외부 리소스를 사용하기 위한 SOP의 예외 조항이 CORS이다.

<br>

# CORS 동작 원리

### Simple request

- 서버에게 바로 요청을 보내는 방법
  - 이 후 서버가 응답 헤더에 Access-Control-Allow-Origin과 같은 값을 보내주면 그때 브라우저가 CORS 정책 위반 여부를 검사하는 방식
    ![단순요청방법](https://evan-moon.github.io/static/d8ed6519e305c807c687032ff61240f8/6af66/simple-request.png)

1. 요청의 메소드는 GET, HEAD, POST 중 하나여야 한다.
2. Accept, Accept-Language, Content-Language, Content-Type, DPR, Downlink, Save-Data, Viewport-Width, Width를 제외한 헤더를 사용하면 안 된다.
3. 만일, Content-Type을 사용한다면 application/x-www-form-urlencoded, multipart/form-data, text/plain만 허용된다.

<br>

### Preflight request

- 요청을 한번에 보내는 것이 아니라 예비 요청과 본 요청으로 나누어서 서버로 전송하는 방법
  - HTTP 메서드 중 하나인 OPTIONS 메서드 사용
    ![프리플라이트](https://evan-moon.github.io/static/c86699252752391939dc68f8f9a860bf/6af66/cors-preflight.png)

<br>

### Credentialed Request

- 인증된 요청을 사용하는 방법
  - CORS의 기본 방식보다는 다른 출처 간 통신에서 좀 더 보안을 강화하고 싶을 때 사용

**credentials 옵션** : 요청에 인증과 관련된 정보를 담을 수 있게 해준다.
| 옵션 값 | 설명 |
| ------------------ | -------------------------------------------- |
| same-origin (기본값) | 같은 출처 간 요청에만 인증 정보를 담을 수 있다 |
| include | 모든 요청에 인증 정보를 담을 수 있다 |
| omit | 모든 요청에 인증 정보를 담지 않는다 |

<br>

# CORS 에러 해결하기

- Access-Control-Allow-Origin 헤더 세팅
  - 명시적인 URL 설정(Access-Control-Allow-Origin: https://xxx.com)
- 프록시 서버 사용
  - 클라이언트에서 외부 서버로 바로 요청하는 것이 아니라 프록시 서버를 사용하여 우회하는 방법

<br>

# 참고

> [교차 출처 리소스 공유 (CORS)](https://developer.mozilla.org/ko/docs/Web/HTTP/CORS)  
> [CORS는 왜 이렇게 우리를 힘들게 하는걸까?](https://evan-moon.github.io/2020/05/21/about-cors/#credentialed-request)  
> [CORS란 무엇인가 ?](https://velog.io/@pilyeooong/CORS%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80)  
> [[Browser] CORS란?](https://beomy.github.io/tech/browser/cors/)  
> [나를 너무나 힘들게 했던 CORS 에러 해결하기](https://xiubindev.tistory.com/115)
