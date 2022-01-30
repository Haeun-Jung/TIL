# 라이프사이클

Vue 컴포넌트는 생성 후 소멸될 때까지 생명주기가 있다. Vue 인스턴스는 크게 4가지 과정을 거친다.

1. **create** : 인스턴스의 생성

2. **mount** : 생성된 인스턴스를 화면에 부착

3. **update** : 화면에 부착된 인스턴스의 내용 갱신

4. **destroy** : 인스턴스가 소멸

![라이프사이클](https://joshua1988.github.io/vue-camp/assets/img/lifecycle.dcbe29f6.png)

<br>

## beforeCreate

beforeCreate는 가장 먼저 실행되는 라이프사이클 훅으로, Vue 인스턴스가 초기화된 직후에 발생된다. 컴포넌트가 DOM에 추가되기 전이기 때문에 `this.$el`에 접근할 수 없다. 또한, `data`와 `methods`에도 접근할 수 없다. data와 이벤트(`$on`, `$once`, `$off`, `$emit`), 감시자(`$watch`) 등이 설정되기 전에 호출된다.

<br>

## created

created 훅에서는 `data`, `computed`, `methods`, `watch` 등이 활성화되어 접근이 가능하다. 하지만 DOM에는 추가되지 않은 상태이기 때문에 `$el`은 사용이 불가능하다. created 단계에서 컴포넌트 초기에 외부에서 받아온 값들로 data를 세팅해야 하거나 이벤트 리스너를 선언하는 것이 가장 적절하다.

<br>

## beforeMount

컴포넌트가 DOM에 추가되기 직전에 호출되는 라이프사이클 훅이다. 렌더링 되고 DOM을 변경해야 한다면 mounted 라이프사이클 훅을 사용하면 되기 때문에, 거의 사용하지 않는다. 서버 사이드 렌더링을 지원하지 않는다.

<br>

## mounted

가상 DOM의 내용이 실제 DOM에 부착되고 난 이후에 실행되므로, `this.$el`을 비롯한 `data`, `computed`, `methods`, `watch` 등 모든 요소에 접근이 가능하다. mounted 훅이 호출되었다고 모든 컴포넌트가 마운트 되었다고 보장할 수 없다. 전체가 렌더링 보장된 상태에서 작업을 하기 위해서는 `$nextTick`을 사용해야 한다. 서버 사이드 렌더링을 지원하지 않는다.

<br>

## beforeUpdate

컴포넌트에서 사용되는 `data`의 값을 변경하고 DOM에도 그 변경을 적용시켜야 할 때가 있는데, beforeUpdate 훅은 변화 직전에 호출된다. 가상 DOM을 렌더링 하기 전이지만, 변경 예정일 값을 이용하여 작업할 수 있다. beforeUpdate 훅에서 값을 추가적으로 변경하여도 렌더링을 추가로 호출하지는 않기 때문에 무한 루프에 빠지지 않는다.

<br>

## updated

가상 DOM을 렌더링하고 실제 DOM이 변경된 후에 호출된다. 변경된 data가 DOM에도 적용된 상태이다. 만약 변경된 값을 DOM을 이용해 접근하고 싶을 때, updated 훅이 가장 적절하다. 하지만 updated 훅에서 `data`를 변경하면 무한 루프에 빠질 수 있다. mounted 훅과 마찬가지로 재 렌더링이 끝났다는 것이 보장된 상태에서 작업하기 위해서는 `$nextTick`을 사용해야 한다.

<br>

## beforeDestroy

컴포넌트가 제거되기 직전에 beforeDestroy 훅이 호출된다. 아직 해체되기 전이므로, 인스턴스는 완전하게 작동하기 때문에 모든 속성에 접근이 가능하다. 이벤트 리스너를 해제하는 등 인스턴스가 사라지기 전에 해야 할 일을 처리하면 된다. 서버 사이드 렌더링을 지원하지 않는다.

<br>

## destroyed

컴포넌트가 제거된 후에 호출되는 라이프사이클 훅이다. 해체가 끝났기 때문에, 인스턴스의 속성에 접근할 수 없다. 또한 하위 Vue 인스턴스도 삭제된다. 서버 사이드 렌더링을 지원하지 않는다.

<br>

## 참고

> [Vue 라이프사이클 이해하기](https://wormwlrm.github.io/2018/12/29/Understanding-Vue-Lifecycle-hooks.html)  
> [[Vue.JS] 라이프 사이클](https://beomy.tistory.com/47)  
> [[Vue.js 시작하기] - 라이프사이클](https://developerjournal.tistory.com/5)
