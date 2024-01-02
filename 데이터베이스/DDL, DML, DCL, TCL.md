### DDL
Data Definition Language, 데이터 정의어

데이터와 데이터간의 관계를 정의하여 데이터베이스 구조를 설정하는 SQL문

데이터베이스, 테이블, 인덱스 등 객체를 생성(**CREATE**)하고, 변경(**ALTER**)하거나 삭제(**DROP**)하는 등의 역할을 수행한다

### DML
Data Minipulation Language, 데이터 조작어

데이터베이스에 저장된 자료를 검색(**SELECT**), 삽입(**INSERT**), 삭제(**DELETE**), 수정(**UPDATE**)하기 위해 사용되는 언어

### DCL 
Data Control Language, 데이터 제어어

데이터베이스에 대한 접근 권한을 부여(**GRANT**)하고 회수(**REVOKE**)하는 작업을 수행하는 언어

데이터의 보안, 무결성, 회복 등을 정의하는 데 사용

### TCL 
Transaction Control Language, 트랜잭션 제어어

 데이터 접근 제어어(DCL)에서 COMMIT, ROLLBACK, SAVEPOINT 연산만을 별도로 분리한 언어
 
 데이터 조작 처리어(DML)에 의하여 조작된 결과를 트랜잭션별로 제어하는 데 사용

 COMMIT : 완수한 작업을 데이터베이스에 영구적으로 반영하는 것
 ROLLBACK : 데이터베이스를 작업 이전 상태로 복구한다
 SAVEPOINT : 저장점을 지정해, ROLLBACK시 트랜잭션 전체가 아닌 저장점까지만 롤백할 수 있게 한다

---
### 출처
[정보통신용어사전](https://terms.tta.or.kr/)
