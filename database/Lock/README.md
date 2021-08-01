## Lock

Lock은 트랜잭션 처리의 순차성, 일관성을 보장해주는 기능을 제공한다.

Lock의 종류는 크게 두가지로 나누어 진다.

### Shared Lock(공유 Lock)

Shared Lock은 데이터를 읽을 때 사용되어지는 Lock이다.

Shared Lock끼리는 동시에 접근이 가능하지만, Exclusive Lock과 함께 사용할 순 없다.

즉, 내가 보고 있는 데이터는 다른 사용자가 볼 수 있지만 변경할 수 없다.

### Exclusive Lock(베타 Lock)

Exclusive Lock은 데이터를 변경하고자 할 때 사용되며 트랜잭션이 완료될 때까지 유지된다.

Exclusive Lock이 해제될 때까지 다른 트랜잭션(읽기 포함)은 해당 리소스에 접근할 수 없다.

또한 Exclusive Lock은 다른 트랜잭션이 수행되고 있는 데이터에 대해서는 함께 Lock을 설정할 수 없다.