# SQL Injection

보안 상의 허점을 이용해, 악의적인 SQL문을 실행되게 함으로써 데이터베이스를 비정상적으로 조작하는 코드 인젝션 공격 방법

OWASP가 선정한 상위 10가지 웹 애플리케이션 보안 위험 중 3위

### 예시 
```sql
# 1=1 이 항상 참이 되므로 password가 틀려도 로그인 가능
SELECT * 
FROM users 
WHERE 
  username='admin' AND 
  password='password' OR 1=1 
```

### 예방
주입을 방지하려면 데이터를 명령 및 쿼리와 별도로 관리

ORM을 사용해 SQL에 직접 접근하지 못하게 하거나 Prepared Statement 사용

<br>
Prepared Statement : 비슷한 쿼리문을 높은 효율성으로 실행하기 위해 사용되는 기능, 템플릿 형태로 특정한 상수값만 매 실행 때마다 대체
ex) `INSERT INTO products (name, price) VALUES (?, ?);`

---
### 출처
[OWASP Top Ten](https://owasp.org/www-project-top-ten/)
[SQL 삽입](https://ko.wikipedia.org/wiki/SQL_%EC%82%BD%EC%9E%85)
[프리페어드 스테이트먼트](https://ko.wikipedia.org/wiki/%ED%94%84%EB%A6%AC%ED%8E%98%EC%96%B4%EB%93%9C_%EC%8A%A4%ED%85%8C%EC%9D%B4%ED%8A%B8%EB%A8%BC%ED%8A%B8)