## 스레드

> 프로세스 내 작업 단위

<br>

## 유저 레벨 스레드

커널 영역의 상위에서 지원되며 **스레드의 기능을 제공하는 라이브러리를 활용**한다. 스레드 간 전환할 때마다 커널 스케줄러를 호출할 필요가 없기 때문에 커널 스레드보다 오버헤드가 적다.

![유저 레벨 스레드](https://t1.daumcdn.net/cfile/tistory/1217D5184B8EF37A3B)

👍 유저모드에서 커널모드로의 전환이 필요없다. 성능이 좋다.  
👎 프로그래밍 하기 어렵고 커널 레벨 스레드에 비해 결과 예측이 어렵다. 프로세스내의 한 스레드가 커널로
진입하는 순간 나머지 스레드들도 전부 정지된다

<br>

## 커널 레벨 스레드

**스레드를 생성 및 스케줄링하는 주체가 커널**이다.  
운영체제 시스템 내에서 생성되어 동작하는 스레드로, 커널이 직접 관리한다.

![커널 레벨 스레드](https://t1.daumcdn.net/cfile/tistory/151B49194B8EF36129)

👍 멀티 프로세서를 활용할 수 있다.  
👎 유저 모드와 커널 모드로의 전환으로 인해 성능이 저하된다.

<br>

## 유저 영역과 커널 영역

![유저/커널 영역](https://t1.daumcdn.net/cfile/tistory/230AFD4256C3EAFF0D)

- **유저 영역** : 사용자가 구현한 프로그램 동작시 사용하게 되는 메모리 영역
- **커널 영역** : 운영체제 동작시 사용하게 되는 메모리 영역

<br>

## 📌 n : 1 매핑

> 사용자 레벨 스레드가 커널 레벨 스레드를 공유하는 매핑

✔ 사용자 스레드가 블록되면 어플리케이션 전체가 중단되는 경우가 생긴다.

![n : 1 매핑](https://blog.kakaocdn.net/dn/4YfjR/btqTcRw5fj0/POVqHqTUCyiGx3wVP8dHXK/img.png)

<br>

## 📌 1 : 1 매핑

> 각각의 사용자 레벨의 스레드가 하나의 커널 레벨 스레드와 연결되는 매핑

![1 : 1 매핑](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcBHRcL%2FbtqTp2XQBeF%2FbDNfKVwqnKo5cxdYbYG3k1%2Fimg.png)

<br>

## 📌 n : m 매핑

> 1개 이상의 커널 레벨 스레드와 1개 이상의 사용자 레벨 스레드가 교차로 연결되는 매핑

✔ n : 1 매핑시 어플리케이션이 중단되는 단점을 보완

![n : m 매핑](https://blog.kakaocdn.net/dn/b4Km2m/btqThZg4pzc/c23azkjJEdfioyj9XpBjTK/img.png)

<br>

## 참고

> https://helloinyong.tistory.com/293  
> https://kspsd.tistory.com/50  
> https://genesis8.tistory.com/242  
> https://sayo-le.tistory.com/67
