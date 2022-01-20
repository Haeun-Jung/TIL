# slice

- slice(start[, end])
- 기존 배열을 변형하지 않고, 새로운 배열을 반환한다.

```javascript
let a = [1, 2, 3, 4, 5];

console.log(a.slice(0, 3)); // [1, 2, 3]
console.log(a); // [1, 2, 3, 4, 5]
```

<br>

# splice

- splice(start[, deleteCount[, item1[, item2[, ...]]]])
- 기존 배열을 변형하고, 새로운 배열을 반환한다.

```javascript
let a = [1, 2, 3, 4, 5];
let b = a.splice(3, 2, "a");

console.log(a); // [1, 2, 3, "a"]
console.log(b); // [4, 5]
```

<br>

# split

- split(separator[, limit])
- String 메서드
- 문자열을 separator 기준으로 나누어 배열로 만든 후, 배열을 반환한다.

```javascript
let a = "1.2.3.4.5";

console.log(a.split(".")); // ["1", "2", "3", "4", "5"]
```

<br>

# 참고

> [[JS/Array] slice()와 splice()의 차이점](https://im-developer.tistory.com/103)  
> [[JavaScript] splice, slice, split](https://eomtttttt-develop.tistory.com/193)
