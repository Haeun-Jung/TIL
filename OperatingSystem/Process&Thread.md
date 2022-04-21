# 📌 프로세스(Process)

**실행 중인 프로그램**으로, 스케줄링의 대상이 되는 작업(task)과 같은 의미를 가진다.

## 특징

    ✔ 프로세스는 각각 독립된 메모리 영역을 할당한다.
    ✔ 기본적으로 프로세스당 최소 1개의 스레드를 가진다.
    ✔ 각 프로세스는 별도의 주소 공간에서 실행된다.
    ✔ 한 프로세스가 다른 프로세스의 자원에 접근하려면 프로세스 간의 통신(IPC, inter-process communication)을 사용해야 한다.
    ✔ Context Switch에 많은 비용이 발생한다.

## 메모리 영역

![프로세스 메모리](https://blog.kakaocdn.net/dn/cqk9Wt/btq9Rehkwfd/6QNk4WEKb7O7JR4TvXakvK/img.png)

## 프로세스의 상태 변화

![프로세스 상태변화](https://t1.daumcdn.net/cfile/tistory/9988343C5BB4601A0B)

- New로 생성 후, Ready Queue에 들어감
- 스케줄러에 의해 Ready <-> Running 변화 발생
- I/O Event 발생시 Running -> Blocked
- Blocked에서 I/O Event 종료시 Ready

<br>

# 📌 스레드(Thread)

**CPU 사용의 기본 단위**로, 프로세스(Process)내에서 실행되는 여러 흐름의 단위를 의미한다.

## 특징

    ✔ 스레드는 프로세스 내에서 각각 Stack 영역만 따로 할당 받고 Code, Data, Heap 영역은 공유한다.
    ✔ 스레드가 여러개 있으면 멀티스레드라 불린다.
    ✔ 멀티스레드에서 각 스레드끼리 프로세스의 일정 메모리를 공유해서 사용한다.
    ✔ 데이터 전송과 Context Switch에 많은 비용이 발생하지 않는다.

<br>

## 📌 [Context Switching](https://github.com/Haeun-Jung/TIL/blob/main/OperatingSystem/Context_Switching.md)

Multi Process 환경에서 CPU가 어떤 하나의 Process를 실행하고 있는 상태에서 인터럽트(Interrupt) 요청에 의해 다음 우선순위의 Process가 실행되어야 할 때 **기존의 Process의 상태/레지스터 값(Context)을 저장하고 CPU가 다음 Process를 수행하도록 새로운 Process의 상태/레지스터 값(Context)를 교체**하는 작업

<br>

## 참고

> https://zangzangs.tistory.com/107  
> https://www.crocus.co.kr/1369  
> https://velog.io/@co_mong/%EB%A9%B4%EC%A0%91-OS
