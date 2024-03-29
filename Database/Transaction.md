# 📌 트랜잭션(Transaction)

**하나의 논리적 기능을 수행하여 완료하기까지의 작업 단위**를 의미한다. 쉽게 말하면, 한 번에 수행되어야 하는 일련의 연산들이다. 트랜잭션은 사용자 혹은 시스템의 오류가 있더라도 데이터베이스에서 데이터를 안정적으로 보장할 수 있도록 해준다. 하나의 트랜잭션은 Commit 되거나 Rollback 된다.

<br>

# 📌 트랜잭션 연산

### Commit

트랜잭션으로 묶인 모든 쿼리가 성공되어, 트랜잭션 쿼리 결과를 데이터베이스에 반영한다.

### Rollback

쿼리 실행 결과를 취소하고 데이터베이스를 트랜잭션 이전 상태로 되돌린다.

### SAVEPOINT

취소하려는 지점을 SAVEPOINT로 명시한 뒤 ROLLBACK TO [SAVEPOINT이름];을 실행하면 작업의 전체가 아닌 특정 부분에서 트랜잭션을 취소할 수 있다.

<br>

# 📌 트랜잭션 연산 과정

![트랜잭션 연산 과정](https://k.kakaocdn.net/dn/PDxus/btqB2uxivzk/ERRntkdAzfbibpUlXmtohK/img.png)

**활성(Active)** : 트랜잭션이 정상적으로 실행 중인 상태

**부분적 완료(Partially Committed)** : 트랜잭션의 마지막 연산까지 실행했지만, Commit 연산이 실행되기 직전의 상태

**완료(Committed)** : 트랜잭션이 성공적으로 종료되어 Commit 연산을 실행한 후의 상태

**실패(Failed)** : 트랜잭션 실행에 오류가 발생하여 중단된 상태

**철회(Aborted)** : 트랜잭션이 비정상적으로 종료되어 Rollback 연산을 수행한 상태

<br>

# 📌 트랜잭션의 성질(ACID)

트랜잭션이 안전하게 수행된다는 것을 보장하기 위한 4가지 성질이 있다. 앞 글자를 따서 `ACID`라고 불린다.

### Atomicity(원자성)

- 트랜잭션의 연산은 데이터베이스에 모두 반영되든지 아니면 전혀 반영되지 않아야 한다.

- 완료되지 않은 트랜잭션의 중간 상태를 데이터베이스에 반영하면 안 된다.

### Consistency(일관성)

- 트랜잭션 실행을 성공적으로 완료하면 언제나 일관성 있는 데이터베이스 상태로 변환한다.
- 시스템이 가지고 있는 고정 요소는 트랜잭션 수행 전과 트랜잭션 수행 완료 후의 상태가 같아야 한다.

### Isolation(독립성)

- 둘 이상의 트랜잭션이 병행 실행되는 경우 어느 하나의 트랜잭션 실행 중에 다른 트랜잭션의 연산이 끼어들 수 없다.

- 수행 중인 트랜잭션은 완전히 완료할 때까지 다른 트랜잭션에서 수행 결과를 참조할 수 없다.

### Durability(영속성)

- 성공적으로 완료된 트랜잭션의 결과는 시스템이 고장 나더라도 영구적으로 반영되어야 한다.

<br>

# 참고

> [https://youtu.be/e9PC0sroCzc](https://youtu.be/e9PC0sroCzc)  
> [https://coding-factory.tistory.com/226](https://coding-factory.tistory.com/226)  
> [https://youtu.be/YuiQ01M2FOs](https://youtu.be/YuiQ01M2FOs)  
> [https://devuna.tistory.com/30](https://devuna.tistory.com/30)
