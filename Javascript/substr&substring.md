# substr

- **string.substr(start[, length])**
- 기존 문자열은 그대로 보존하고, length 값이 음수일 경우 빈 값을 반환한다. 

```javascript
let str = 'github HaEunJung';
console.log(str.substr(7));       // "HaEunJung"
console.log(str.substr(7, 5));    // "HaEun"
console.log(str.substr(-4));      // "Jung", 음수인 경우 뒤에서부터 카운팅
console.log(str.substr(-4, 2));   // "Ju"
console.log(str.substr(1, -2));   // ""
```

<br>

# substring

- **string.substring(start[, end])**
- 기존 문자열은 그대로 보존하고, start 인덱스부터 end 인덱스 바로 앞까지 반환한다.
- start가 end보다 크다면 작은 숫자가 시작 위치로, 큰 숫자가 종료 위치로 설정된다.
- 매개변수 둘 중에 한개 값이 음수값이라면 시작 위치가 0으로 설정된다.
- 매개변수가 둘 다 음수일 경우 빈 값을 반환한다. 

```javascript
let str = 'github HaEunJung';
console.log(str.substring(0));      // "github HaEunJung"
console.log(str.substring(0, 6));   // "github"
console.log(str.substring(6, 0));   // "github"
console.log(str.substring(6, 2));   // "thub"
console.log(str.substring(0, -4));  // ""
console.log(str.substring(2, -2));  // "gi"
console.log(str.substring(-1, -2)); // ""

```

<br>

# 참고

> https://webclub.tistory.com/20
