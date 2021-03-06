## Clustered Index, Secondary Index

Clustered index는 테이블당 한 개만 생성할 수 있고, Secondary Index는 테이블당 여러 개를 생성할 수 있다. 또, Clustered Index는 행 데이터를 인덱스로 지정한 열에 맞춰서 자동 정렬한다.

UNIQUE에 NOT NULL이 포함되면 Clustered Index로 지정된다.

MySQL에서 Index는 기본적으로 B-Tree 구조를 사용하는데, 이 구조는 데이터를 검색할 때 아주 뛰어난 성능을 발휘한다.

B-Tree 구조는 루트 페이지, 리프 페이지로 구성 되어 있다. 루트 페이지를 검색한 후 해당 데이터 정보를 찾아 리프 페이지로 직접 이동한다.

하지만 B-Tree 구조가 마냥 좋은 것만은 아니다. 

B-Tree 구조는 데이터 변경 작업(insert, update, delete) 시에 성능이 나빠지는 단점이 있다. 그 이유는 '페이지 분할' 작업이 발생되기 때문이다.

Clustered Index는 루트 페이지와 리프 페이지(중간 페이지가 있다면 중간 페이지도 포함)로 인덱스가 구성되어 있으며 동시에 인덱스 페이지의 리프 페이지는 데이터 그 자체이다.

Secondary Index는 데이터 페이지를 건드리지 않고, 별도의 장소에 인덱스 페이지를 생성한다. 우선, 인덱스 페이지의 리프 페이지에 인덱스로 구성한 열을 정렬한다. 그리고 데이터 위치 포인터를 생성한다.
데이터의 위치 포인터는 Clustered Index와 달리 주소값(페이지 번호 + #오프셋)이 기록되어 바로 데이터의 위치를 가리키게 된다.

Secondary Index는 데이터 페이지를 정렬하는 것이 아니므로, 그냥 데이터 페이지의 뒤쪽 빈 부분에 삽입된다. 그리고 인덱스의 리프 페이지에도 약간의 위치가 조정된 것일뿐 페이지 분할은 일어나지 않는다.
결국, Clustered Index보다 데이터 입력에서는 성능에 주는 부하가 더 적다.

