# 관계형 Database
**키(key)와 값(value)들의 간단한 관계를 테이블화시킨 전산정보 데이터베이스**로, 각각의 테이블이 서로 관계를 맺는다.

`Table` : `Row` + `Column` + `Schema`


![관계형DB](https://mblogthumb-phinf.pstatic.net/MjAxODAxMTZfMjA3/MDAxNTE2MDU2NDg4MTcx.vEJiQWwws9BgQ1mC0-m0_rWVon_Zs750OPFfrnAUVfUg.gKMBxYPtdUiCx6TIzYMeLjBofB5l8Bfq_8JtGJCuzwog.PNG.qbxlvnf11/20180112_181314_%281%29.png?type=w800)

### 열(Column)
- 항목의 속성(명칭)
- 각각 정수, 텍스트 같은 데이터 유형 지정

### 행(Row)
- 각 데이터 항목 저장

### 스키마(Schema)
- 필드는 데이터 유형과 제약 사항을 지정할 수 있는데 이러한 제약 사항을 스키마라고 한다.
- `unique`, `not null` 등의 제약 사항 지정

<br>

## [정규화](https://github.com/Haeun-Jung/TIL/blob/master/Database/정규화.md)  
**테이블을 분리하고, 중복 데이터를 제거하는 과정**
- 불필요한 데이터 제거, 중복 최소화
- 각종 이상 현상 방지

<br>

## 참고
> https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=qbxlvnf11&logNo=221186206129
