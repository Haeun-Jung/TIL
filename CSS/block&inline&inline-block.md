# block
무조건 한줄을 점유하고, 다음 태그는 무조건 줄바꿈이 적용된다.

<br/>

# inline
text 크기만큼만 공간을 점유하고, 줄바꿈을 하지 않는다.
- width/height 적용불가
- margin/padding-top/bottom 적용불가
- line-height를 원하는대로 사용할 수 없다.

<br/>

## 비교
|   |block|	inline|
|---|---|---|
|줄바꿈|	줄바꿈 O, 새로운 라인에서 시작한다.|줄바꿈 X, 새로운 라인에서 시작하지 않는다.|
|요소 너비|	사용 가능한 전체 너비를 차지한다.|컨텐츠 너비 만큼의 너비를 차지한다.|
|높이 및 너비|	높이(height)과 너비(width) 크기 설정 가능하다.|높이(height)와 너비(width) 설정 불가능하다. 컨텐츠 만큼의 크기를 차지하기 때문이다.|
|상하 마진|상하 마진(margin-top, margin-bottom)을 가질 수 있다.|상하 마진(margin-top, margin-bottom)을 가질 수 없다. 좌우 마진만 가능하다.|
|컨텐츠|	inline, block 요소를 컨텐츠로 가질 수 있다.|block 요소를 컨텐츠로 가질 수 없다. (데이터 또는 inline 요소만 가능)|
|대표적인 요소|div, p, h1~h6, ul, ol|span, a, small, big, strong|

<br/>

## inline-block
inline-block은 inline속성과 block속성의 특징을 둘다 가지고 있다. inline속성과 다르게 width,height 적용 가능하고 line-height를 커스텀하게 적용할 수 있다.

<br/>

## 참고
> https://sunnykim91.tistory.com/121  
> https://jinnynote.com/learn/web/display-block-vs-inline/  
> https://ruden91.github.io/blog/inline-vs-block-vs-inline-block/
