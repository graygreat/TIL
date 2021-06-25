# 프로젝트 리뷰

## COLLATE utf8mb4_0900_ai_ci의 의미

* utf8mb4: 각 character는 최대 4byte의 UTF-8 인코딩을 지원
* 0900: Unicode의 collation algorithm 9.0.0을 지원
* ai: accent insensitivity (알파벳과 비슷한 특수문자도 알파벳으로 인식)
* ci: case insensitivity (소문자 대문자의 순서가 같음)

COLLATE utf8mb4_0900_ai_ci을 사용하게 되면 정렬에 영향을 줄 수 있고 뿐만 아니라 다개국어 데이터가 있는 큰 DB에서 Index, Unique, Primary key에 영향을 줍니다.

