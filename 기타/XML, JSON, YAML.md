### XML
eXtensible Markup Language
데이터를 정의하는 규칙을 제공하는 마크업 언어

자체적으로 컴퓨팅 작업을 수행할 수 없는 대신 구조적 데이터 관리를 위해 모든 프로그래밍 언어 또는 소프트웨어를 구현

HTML과 같이 **<태그>** 형식 사용
```XML
<?xml  version="1.0"?>
<post>
  <title>Hello</title>
  <author>Sang</author>
  <body>World</body>
</post>
```
### JSON
자바스크립트의 객체 표기법으로부터 파생된 부분 집합

간결하고 작성하기 쉽기 때문에 많이 사용

문법 오류에 취약 (콤마 하나가 잘못되어도 문서 전체를 해석할 수 없다)
```json
{
    "post": {
        "title": "Hello",
        "author": "Sang",
        "body": "World"
    }
}
```

### YAML
YAML Ain't Markup Language or Yet Another Markup Language
사람이 읽을 수 있는 데이터 직렬화 언어로서, 구성 파일 작성에 자주 사용

json에 비해 간결하다


```yaml
post:
  title: Hello
  author: Sang
  body: World
```


	
||XML|JSON|YAML|
|--|--|--|--|
의미|Extensible Markup Language|JavaScript Object Notation|YAML Ain't Markup Language
|용도|데이터를 저장하고 전송하기 위한 마크업 언어로 태그를 사용해 데이터를 구조화하고 표현하는데 사용|애플리케이션과 서비스 간에 정형 데이터를 교환하기 위한 데이터 직렬화 형식<br> 사람이 사용하는 것보다 애플리케이션에 우선적으로 사용|소프트웨어 애플리케이션과 서비스 간에 정형 데이터를 교환하기 위한 데이터 직렬화 형식<br>애플리케이션보다 사람이 더 많이 사용|
|주요 사용사례|여러 데이터 유형을 여러 변수와 함께 저장하려는 경우 사용|플랫폼, 언어, 분산 소프트웨어 통신, 웹 앱, 구성 파일 및 API에 널리 사용|자동화, DevOps,코드형 인프라(IaC) 도구 및 서비스의 구성 파일에 사용|
|가독성|어렵다|쉽다|가장 쉽다|
|데이터 유형|XML은 모든 JSON 데이터 유형과 부울, 날짜, 이미지 및 네임스페이스와 같은 추가 유형을 지원|숫자, 부울, Null, 문자열, 배열, 객체|시퀀스, 스칼라 및 매핑으로 구성된 중첩된 데이터 모음을 통해 모든 데이터 유형을 지원|
|주석 지원|O|X|O|

---
### 출처
[]()