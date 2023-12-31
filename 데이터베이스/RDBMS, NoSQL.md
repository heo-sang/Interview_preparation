# 데이터베이스
통합하여 관리되는 데이터의 집합

### RDBMS
Relational DataBase Management System, 관계형 데이터베이스 관리 시스템
데이터를 열과 행으로 이뤄진 테이블 형태로 관리하는 시스템
- 테이블의 구조와 데이터 타입 등이 사전에 정의되고 수정이 어렵다
- SQL(Structured Query Language)을 이용해 데이터를 조작
- 데이터가 관계를 통해 여러 테이블에 분산된다(외래키를 사용해 테이블들을 join)

##### 장점
- 데이터의 무결성 보장
- 데이터를 중복없이 저장할 수 있다

##### 단점
- 시스템이 크면 join문이 많은 복잡한 쿼리로 인해 성능이 저하될 수 있다
- 스키마 변경이 어렵다
- 수평확장이 힘들어 상대적으로 비싸다.

##### 사용
- 관계를 맺고 있는 데이터가 자주 변경되는 시스템의 경우
- 명확한 스키마가 필요한 경우
- ACID가 보장되어야 할 때

### NoSQL
비관계형 데이터베이스로 테이블과는 다른 형태로 데이터를 저장(키값, 그래프, 도큐먼트 등)

![nosql](../image/nosql.png)

- **키,값** : 키에 값을 맵핑하는 해시 구조
  - 값은 어떠한 형태의 데이터라도 담을 수 있다
  - 질의의 속도가 빠르다
  - 값의 내용을 사용한 쿼리는 불가능

- **도큐먼트** : 데이터를 키와 도큐먼트의 형태로 저장
  - 값이 계층적인 형태인 도큐먼트로 저장된다는 점이 키값구조와 다르다
  
- **그래프** : 데이터는 연속적인 노드, 관계, 특성의 형태로 저장
  - 관계형 모델에 가깝고 ACID 트랜잭션을 지원
  - 질의는 그래프 순회를 통해 이루어진다.

##### 장점
- 수평확장이 쉽다
- 데이터에 새로운 필드를 추가할 수 있다
- 자유로운 데이터 구조

##### 단점
- 데이터 중복 발생 가능
- 명확한 데이터 구조를 보장하지 않는다
- 일관성이 떨어진다

##### 사용
- 정확한 데이터구조를 모르거나 확장될 가능성이 있는경우
- 대용량 처리를 해야하는 경우
- 로그 저장 용도

---
### 출처
[NoSQL](https://namu.wiki/w/NoSQL)