## ACID

ACID는 Transaction이 안전하게 수행된다는 것을 보장하기 위한 특징이다.

### Atomicity(원자성)

DB에 모두 반영되거나, 전혀 반영되지 않아야 한다. (All or Nothing)

### Consistency(일관성)

DB 상태가 일관된 상태였다면 트랜잭션 작업이 종료된 후에도 일관성 있는 상태를 유지해야한다.

### Isolation(독립성)

둘 이상의 트랜잭션이 동시 실행되고 있을 때, 각각의 Transaction은 독립적으로 이루어져 어떤 트랜잭션도 다른 Transaction 연산에 끼어들 수 없다.

### Durability(지속성, 영구성)

트랜잭션이 성공적으로 완료되었으면 결과는 영구히 반영되어야 한다.