### **Queue**
  - 단순히 put과 get으로 넣고, 가장 먼저 들어왔던 요소를 빼주는 기능만을 지원
  -  Queue 모듈은 멀티스레드 환경을 지원(여러 스레드가 동시에 큐를 사용하더라도 문제가 없게 추가 작업을 수행, 따라서 deque보다 느리다.)


### **deque** : `double-ended queue`의 줄임말로, 앞과 뒤, 즉 양방향에서 데이터를 처리할 수 있는 queue형 자료구조를 의미한다. 스택과 큐의 기능을 모두 가졌다.
  - FIFO, LILO 모두 구현
  - 각 명령을 O(1)으로 지원

<br>

## 참고
> https://programming119.tistory.com/184  
> https://jungeun960.tistory.com/148  
> https://www.acmicpc.net/board/view/49166
