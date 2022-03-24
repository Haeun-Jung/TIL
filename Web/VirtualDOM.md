# Virtual DOM(Document Object Model)
DOM과 유사한 객체를 메모리에 올려놓고, 변경 사항이 생기면 Virtual DOM을 바꾸고, 실제 DOM에서는 변경 사항만 변경할 수 있게 하여 더 반응성이 빠른 웹을 구현할 수 있다.
![Virtual DOM](https://elmprogramming.com/images/chapter-5/5.3-virtual-dom/elm-runtime-virtual-dom.svg)
> Virtual DOM은 DOM이 생성되기 전, 이전 상태 값과 수정사항을 비교하여 달라진 부분만 DOM에게 한 번에 전달하여 딱 한 번만 렌더링을 진행한다.
> DOM이 직접 변경된다면 사소한 변경에도 전체가 재렌더링 되기 때문에 브라우저에 과부하가 올 수 있다. 따라서 최대한 DOM에 직접 접근하지 말아야 한다.

<br/>

## 특징
- DOM의 가벼운 복사본
- in-memory에 존재해서 실제 렌더 되지 않음
- JavaScript 객체로 이루어진 tree data structure
- React와 같은 UI 라이브러리에 널리 쓰임

<br/>

## 참고
> https://programming119.tistory.com/236?category=930152   
> https://velog.io/@sbinha/React%EC%97%90%EC%84%9C-Virtual-DOM  
> https://www.howdy-mj.me/dom/what-is-dom/  
> https://elmprogramming.com/virtual-dom.html
