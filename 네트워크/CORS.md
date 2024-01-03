# CORS
Cross Origin Resource Sharing

브라우저를 통해 웹 서버에서 다른 도메인간 리소스 접근을 허용하도록 하는 웹 브라우저 기술

브라우저에서는 보안적인 이유로 동일 출처(same-origin) 에서만 리소스를 공유할 수 있다
-> cross-origin 요청을 하려면 서버의 동의가 필요 
-> 서버의 리소스 접근을 허용해주는 새로운 HTTP 헤더를 추가하는 방식으로 동작

cross-origin : URL에서 **프로토콜, 호스트, 포트**까지를 origin이라 하는데 이중 하나라도 다를 경우 cross-origin

```yaml
http://127.0.0.1:8080/user/1?q=test

Protocol : http
Host : 127.0.0.1
Port : 8080
Path : /user
QueryString : ?q=test
```

```yaml
# 헤더에 추가해 해당 도메인에 대해서만 리소스 접근 허용
Access-Control-Allow-Origin: http://example.com:8080 http://foo.example.com
```

CORS를 통해서, 기존에 같은 도메인인 경우만 가능했던 ajax 통신이 가능하다

```java


// 특정 컨트롤러에만 CORS 적용하고 싶을때.
@Controller
@CrossOrigin(origins = "*", methods = RequestMethod.GET) 
public class customController {
	// 특정 메소드에만 CORS 적용 가능
    @GetMapping("/url")  
    @CrossOrigin(origins = "*", methods = RequestMethod.GET) 
    @ResponseBody
    public List<Object> findAll(){
        return service.getAll();
    }
}
```

---
### 출처
[정보통신용어사전 CORS](https://terms.tta.or.kr/dictionary/dictionaryView.do?word_seq=097183-1)
[악명 높은 CORS 개념 & 해결법 - 정리 끝판왕](https://inpa.tistory.com/entry/WEB-%F0%9F%93%9A-CORS-%F0%9F%92%AF-%EC%A0%95%EB%A6%AC-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95-%F0%9F%91%8F#%EC%B6%9C%EC%B2%98origin_%EB%9E%80?)