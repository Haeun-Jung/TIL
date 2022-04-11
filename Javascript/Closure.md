# 클로저(Closure)
외부 함수보다 중첩 함수가 더 오래 유지되는 경우, 중첩 함수는 이미 생명 주기가 다한 외부 함수의 변수를 참조할 수 있으며, 이러한 중첩 함수를 "클로저"라고 한다. Javascript에서 클로저는 함수가 생성될 때마다 생성된다. 클로저를 사용하여 객체지향 프로그래밍의 정보 은닉과 캡슐화 같은 이점들을 얻을 수 있다.

```javascript
  function closureF(){  
    let name = 'haeun';  
    return function(){  
      return name;  
    };  
  }  
  let closure = closureF();  
  console.log(closure()); // 'haeun' 출력  
```

> closureF 함수가 종료되었음에도 name에 저장된 값이 그대로 출력된다.

<br/>

## 참고
> https://velog.io/@wkahd01/%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%94%EB%93%9C-%EB%A9%B4%EC%A0%91-%EB%AC%B8%EC%A0%9C-%EC%9D%80%ED%96%89-HTML-%EC%A7%88%EB%AC%B8-%EB%8B%B5%EB%B3%80  
> https://developer.mozilla.org/ko/docs/web/javascript/closures  
