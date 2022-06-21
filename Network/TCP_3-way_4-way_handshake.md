# TCP

**전송 계층에서 사용하는 프로토콜**로, 장치들 사이에 논리적인 접속을 성립하기 위하여 연결을 설정하여 **신뢰성을 보장**하는 연결형 서비스

<br>

## 3-way handshake

TCP 통신을 이용하여 데이터를 전송하기 위해 **네트워크 연결을 설정하는 과정**

![3-way](https://gmlwjd9405.github.io/images/network/3-way-handshaking.png)

    1️⃣ A > B : SYN
    ✔ A가 연결 요청 메세지 전송(SYN)

    2️⃣ B > A : SYN + ACK
    ✔ B가 요청 수락, SYN 패킷 전송

    3️⃣ A > B : ACK
    ✔ 수락 확인(ACK)을 보내 연결을 맺기
    ✔ 해당 단계에서 데이터 전송 가능

<br>

## 4-way handshake

TCP의 **연결을 해제하는 과정**

![4-way](https://gmlwjd9405.github.io/images/network/4-way-handshaking.png)

    1️⃣ A > B : FIN
    ✔ A가 연결을 종료하겠다는 FIN 플래그 전송

    2️⃣ B > A : ACK
    ✔ B의 확인 메세지(ACK)
    ✔ B는 통신이 종료될 때까지 대기
    ✔ 전송할 데이터가 남아있다면 이어서 전송

    3️⃣ B > A : FIN
    ✔ B가 통신이 종료되면, 종료에 합의한다는 의미로 FIN 플래그 전송

    4️⃣ A > B : ACK
    ✔ A의 확인(ACK)

<br>

## 참고

> https://velog.io/@averycode/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-TCPUDP%EC%99%80-3-Way-Handshake4-Way-Handshake  
> https://gmlwjd9405.github.io/2018/09/19/tcp-connection.html  
> https://bangu4.tistory.com/74
