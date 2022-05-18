# useEffect()
**컴포넌트가 렌더링될 때마다 특정 작업을 실행할 수 있도록 하는 Hook**
> 콜백 함수를 가지며, Dependency는 있을 수도 없을 수도 있다.

<br/>

## 실행 조건
✔ 페이지가 처음 렌더링 되고 난 후 무조건 실행  
✔ useEffect에 배열로 지정한 useState의 값이 변경되면 실행

<br/>

## 3가지의 방법
1️⃣ Dependency가 없는 방법
```javascript
useEffect(()=>{});
```
2️⃣ 대괄호를 이용하는 방법
```javascript
useEffect(()=>{}, []);
```
3️⃣ 대괄호 안에 특정 변수를 지정하는 방법
```javascript
useEffect(()=>{}, [특정 변수 혹은 오브젝트]);
```

<br/>

## 참고
> https://ko-de-dev-green.tistory.com/18  
> https://xiubindev.tistory.com/100
