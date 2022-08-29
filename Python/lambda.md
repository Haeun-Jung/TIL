# 람다 표현식(lambda expression)
> 식 형태 `lambda 매개변수 : 표현식` 

람다 표현식은 함수를 간편하게 작성할 수 있으며, 다른 함수의 인수로 넣을 때 주로 사용한다.

```py
# 일반 함수
def solve(x, y):
  return x + y
print(solve(10, 20)) # 30

# 람다
print((lambda x, y: x + y)(10, 20)) # 30
```

![lambda](https://dojang.io/pluginfile.php/13854/mod_page/content/3/032001.png)

```py
print(list(map(lambda x: x + 10, [1, 2, 3]))) # [11, 12, 13]
```

<br>

## 참고
> https://dojang.io/mod/page/view.php?id=2359  
> https://wikidocs.net/64
