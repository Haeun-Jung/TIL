# RESTful API

REST란 REpresentational State Trasfer의 약어로 웹을 이용할 때 제약 조건들을 정의하는 소프트웨어 아키텍처 스타일이다. HTTP URL을 통해 자원(Resource)을 명시하고 HTTP Method(GET, POST, PUT, DELETE)를 통해서 해당 자원(URL)에 대한 CRUD(Create, Read, Update, Delete)를 적용하는 것을 의미한다. 한마디로 HTTP의 장점을 살리고자 하는 통신 규약이라 할 수 있다.

- **GET** : 지정된 URL에서 리소스의 표현을 조회
- **POST** : 지정된 URL에 신규 리소스를 생성
- **PUT** : 지정된 URL에 리소스를 생성하거나 수정
- **PATCH** : 리소스 부분 수정
- **DELETE** : 지정된 URL의 리소스를 제거

<br>

# REST API

REST 기반으로 서비스 API를 구현한 것이다. 최근 OpenAPI(누구나 사용할 수 있도록 공개된 API: 구글 맵, 공공 데이터 등), 마이크로 서비스(하나의 큰 애플리케이션을 여러 개의 작은 애플리케이션으로 쪼개어 변경과 조합이 가능하도록 만든 아키텍처) 등을 제공하는 업체 대부분은 REST API를 제공한다.

> API(Application Programming Interface) : 데이터와 기능의 집합을 제공하여 컴퓨터 프로그램간 상호작용을 촉진하며, 서로 정보를 교환가능 하도록 하는 것

### 특징

- 사내 시스템들도 REST 기반으로 시스템을 분산해 확장성과 재사용성을 높여 유지보수 및 운용을 편리하게 할 수 있다.
- REST는 HTTP 표준을 기반으로 구현하므로, HTTP를 지원하는 프로그램 언어로 클라이언트, 서버를 구현할 수 있다.
- 즉, REST API를 제작하면 델파이 클라이언트 뿐 아니라, 자바, C#, 웹 등을 이용해 클라이언트를 제작할 수 있다.

<br>

## 참고
> https://cocoon1787.tistory.com/540  
> https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html
