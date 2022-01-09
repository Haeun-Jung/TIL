# 뷰 인스턴스에서의 this

## 일반적인 자바스크립트에서의 this

```
var obj = {
    num: 10,
    getNumber: function() {
        console.log(this.num);  // 10
    }
}
```

- 일반적으로 객체의 인스턴스를 가져올 때 this 키워드를 사용한다. this를 내부에서 obj 변수처럼 활용하는 것

<br>

## 메서드 함수 안에서 this는 해당 data 영역을 바라본다.

```
var Vue = {
    el: '',
    data: {
        num: 10,
    }
    methods: {
        getNumber: function() {
           console.log(this.num);  // 10
        }
    }
}
```

<br>

# 참고

> [Vue.js 시작하기 - Age of Vue.js](https://www.inflearn.com/course/Age-of-Vuejs)  
> [[Vue.js] 뷰 인스턴스에서의 this 키워드(data)](https://sas-study.tistory.com/293)
