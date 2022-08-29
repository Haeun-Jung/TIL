### **Queue**
  - 단순히 put과 get으로 넣고, 가장 먼저 들어왔던 요소를 빼주는 기능만을 지원
  -  Queue 모듈은 멀티스레드 환경을 지원(여러 스레드가 동시에 큐를 사용하더라도 문제가 없게 추가 작업을 수행, 따라서 deque보다 느리다.)


### **deque**
  - FIFO, LILO 모두 구현
  - 각 명령을 O(1)으로 지원

<br>

## 참고
> https://programming119.tistory.com/184  
> https://www.acmicpc.net/board/view/49166
