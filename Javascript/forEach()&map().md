# forEach()

```
const array = [1, 2, 3];
const result = array.forEach((num, index) => {
	return num += 1;
})

console.log(result);     // undefined
```

배열의 각 요소에 대해 callback을 실행한다.

<br>

# map()

```
const array = [1, 2, 3];
const result = array.map((num, index) => {
	return num += 1;
})

console.log(result);    // result = [2, 3, 4];
```

배열의 각 요소에 대해 callback을 실행한다. 기존 배열을 건들지 않고, 실행 결과에 따라 동일한 사이즈의 새로운 배열을 반환한다.

<br>

# 결론

- 둘의 공통점은 배열을 순회하며 인자로 전달한 원소의 값을 가지고 함수 로직을 구현한다는 점이다. 또한, 배열을 순회하므로 중간에 break를 사용할 수 없다.(break은 for()에서 사용)
- **return 값의 여부**에 따른 차이점이 있다.
- forEach()는 원소의 값을 활용해서 원소들의 합/평균을 구하거나 기존 배열과 길이가 다른 배열을 받고 싶을 때 사용을 권장한다.
- map()은 어떠한 배열을 순회하며 원소의 값들을 각각 가공하여 새로운 배열을 return 받고 싶을 때 사용을 권장한다.

<br>

# 참고

> [JS Object에서 .forEach 루프와 .map() 루프 사이의 주요 차이점](https://fathory.tistory.com/31)  
> [[JS #1] 자바스크립트 배열 메서드 1: forEach, map](https://medium.com/@hongkevin/js-1-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%B0%B0%EC%97%B4-%EB%A9%94%EC%84%9C%EB%93%9C-1-foreach-map-b1cb1c2237d1)  
> [[JavaScript] for vs. forEach vs. map](https://m.blog.naver.com/wideeyed/221877912230)
