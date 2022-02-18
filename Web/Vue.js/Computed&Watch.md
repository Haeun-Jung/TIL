# Computed

Computed는 템플릿의 데이터 표현을 더 직관적이고 간결하게 도와주는 속성이다.

<br>

### ☑️ 특징

Computed 속성은 종속 대상에 따라 캐싱된다. Computed 속성은 **반응형 종속성 중 일부가 변경된 경우에만 재평가**된다. 데이터가 변경되지 않는다면 Computed 속성에 대해 여러 번 접근하더라도 함수를 다시 실행할 필요 없이 이전에 계산된 결과를 즉시 반환한다. 하나의 Computed에는 하나의 종속성을 가지게 하는 것이 좋다. Computed는 기본적으로 getter이지만, 필요하다면 setter도 제공한다.

<br>

### ❗ 주의사항

- 인자를 받지 않는다.
  - 템플릿에 선언한 Computed 속성에 괄호가 생기면 해당 템플릿을 실제 DOM으로 변환할 때 라이브러리에서 에러를 발생시킨다.
- HTTP 통신 코드를 제외한다.
  - HTTP 통신과 같이 브라우저 리소스가 많이 할애되는 코드는 watch나 methods에 넣는 것이 적합하다.

<br>

# Watch

Watch는 Vue 인스턴스의 특정 프로퍼티가 변경될 때 지정한 콜백 함수가 실행되는 속성이다. **데이터 변경에 대한 응답으로 비동기식 또는 시간이 많이 소요되는 조작을 수행하려는 경우에 가장 유용**하다.

- 다른 데이터 기반으로 변경할 필요가 있는 데이터가 있다면, 명령적인 Watch 콜백보다 Computed 속성을 사용하는 것이 더 좋다.

<br>

## 참고

> [Computed 속성과 Watch](https://v3.ko.vuejs.org/guide/computed.html#computed-%E1%84%89%E1%85%A9%E1%86%A8%E1%84%89%E1%85%A5%E1%86%BC)  
> [computed 속성](https://joshua1988.github.io/vue-camp/syntax/computed.html#computed-%E1%84%89%E1%85%A9%E1%86%A8%E1%84%89%E1%85%A5%E1%86%BC-%E1%84%8B%E1%85%A8%E1%84%89%E1%85%B5)  
> [[Vue.js] watch와 computed 의 차이와 사용법](https://blog.jeongwoo.in/vue-js-watch%EC%99%80-computed-%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%99%80-%EC%82%AC%EC%9A%A9%EB%B2%95-e2edce37ec34)  
> [computed와 watch](https://kr.vuejs.org/v2/guide/computed.html)
