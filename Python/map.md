# map(function, iterable)
**리스트의 요소를 지정된 함수로 처리해주는 함수**로, 원본 리스트를 변경하지 않고 새 리스트를 생성한다. map 객체는 인덱싱이 불가하다.  
`list(map(함수, 리스트))`  
`tuple(map(함수, 튜플))`

```py
# for 사용
a = [1.2, 2.5, 3.7, 4.6]
for i in range(len(a)):
  a[i] = int(a[i])
print(a) # [1, 2, 3, 4]


# map 사용
a = [1.2, 2.5, 3.7, 4.6]
a = list(map(int, a))
print(a) # [1, 2, 3, 4]
```
![map](https://dojang.io/pluginfile.php/13699/mod_page/content/3/022019.png)

```py
# 함수 적용
def game_result(x):
    if x == '가위':
        return 'win'
    elif x == '보':
        return 'draw'
    else:
        return 'lose'

game_list = ['가위', '바위', '보', '가위', '안냄']

result = list(map(game_result, game_list)) # ['win', 'lose', 'draw', 'win', 'lose']
```


<br>

## 참고
> https://dojang.io/mod/page/view.php?id=2286  
> https://jimmy-ai.tistory.com/50
