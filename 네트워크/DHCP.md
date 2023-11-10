# DHCP
Dynamic Host Configuration Protocol
IP 주소, 서브넷 마스크 등의 네트워크 정보와 DNS 주소를 자동으로 설정하기 위해 사용하는 프로토콜

-  IP가 자동으로 관리되므로 설정정보 오류나 중복 할당같은 문제를 예방할 수 있다

### 동작방식

임대(lease)과정

1. **DHCP Discover** : DHCP 클라이언트는 DHCP서버를 찾기위해 DHCP 메시지를 브로드캐스트로 전송
2. **DHCP Offer** : 1을 수신한 서버는 클라이언트에 할당할 IP주소, 서브넷, 게이트웨이, DNS 정보, LEASE TIME등의 정보를 포함한 메시지를 클라이언트로 전송
3. **DHCP Request** : 서버로부터 받은 IP 주소와 DHCP 서버정보를 포함한 요청 메시지를 브로드캐스트로 전송
4. **DHCP Acknowledgement** : 클라이언트로부터 IP를 사용하겠다는 요청을 받으면 해당 IP를 어떤 클라이언트가 언제부터 사용했는지 정보를 기록하고 request 메시지를 정상적으로 수신했다고 응답

- IP를 할당 받는 과정이므로 패킷을 정상적으로 주고받을 수 없어 UDP 사용

- 현재 클라이언트가 IP를 사용하는 경우 갱신과정을 거쳐 IP 주소가 반환 되지 않고 사용 가능


---
### 출처
[IT 엔지니어를 위한 네트워크 입문](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=254155831)