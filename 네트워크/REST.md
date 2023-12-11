# REST
Representational State Transfer
네트워크 리소스를 정의하고 처리하는 방법을 설명하는 일련의 원칙(제약)을 기반으로 하는 **아키텍처 디자인** (**프로토콜이나 표준이 아니다**)

**REST API** : REST 아키텍처 스타일을 따르는 API

### 조건

1. 인터페이스 일관성 : 일관적인 인터페이스로 분리되어야 한다
2. 무상태(Stateless): 서버가 이전의 요청과 독립적으로 클라이언트 요청을 처리
3. 캐시 가능성(Cacheable): 서버 응답 시간을 개선하기 위해 캐싱을 지원
4. 계층화(Layered System): 중개 서버(게이트웨이, 프록시)나 로드 밸런싱 등의 기능을 사용하여 확장성 있는 시스템을 구성
5. Code on demand (optional) - 자바 애플릿이나 자바스크립트의 제공을 통해 서버가 클라이언트가 실행시킬 수 있는 로직을 전송하여 기능을 확장시킬 수 있다
6. 클라이언트/서버 구조 : 자원이 있는 서버, 자원을 요청하는 클라이언트의 구조

### 구성
|구성	|설명|
|--|--|
|자원(Resource)|모든 자원에 고유한 ID가 존재하고, 이 자원은 Server에 존재<br>자원을 구별하는 ID는 '/groups/:group_id'와 같은 HTTP URI <br>Client는 URI를 이용해서 자원을 지정하고 해당 자원의 상태(정보)에 대한 조작을 Server에 요청|
|행위(Verb)|HTTP 프로토콜의 Method 사용<br>HTTP 프로토콜은 GET, POST, PUT, DELETE 와 같은 메서드 제공|
표현(Representation)| Client가 자원의 상태(정보)에 대한 조작을 요청하면 Server는 이에 적절한 응답(Representation)을 회신<br>REST에서 하나의 자원은 JSON, XML, TEXT, RSS 등 여러 형태로 표현<br>일반적으로 JSON이나 XML 이용|

ex)
```java 
//유저 정보 출력
GET  https://localhost:8080/users
```



---
### 출처
[Service Architecture REST](https://www.service-architecture.com/articles/web-services/representational-state-transfer-rest.html)
[REST란 무엇인가요?](https://docs.aws.amazon.com/ko_kr/appsync/latest/devguide/what-is-rest.html)