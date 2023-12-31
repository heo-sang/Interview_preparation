# TCP, UDP
4계층(전송계층)에서 동작하는 프로토콜
- IP에 의해 전달되는 패킷의 오류를 검사하고 재전송 요구 등 제어를 담당하는 계층
![tcp_udp](../image/tcp_udp.png)

### TCP
- 패킷에 번호(SYN)를 부여하고 잘 전송 되었는지에 대해 응답(ACK)한다
- 한번에 얼마를 보내야 사용자가 잘 처리하는지 전송크기(Window size)도 고려한다
- 높은 신뢰성 보장
- 흐름 제어 및 혼잡 제어

안전한 통신을 위해 3way handshake 사용(목적지와 수신지를 확실히 하여 정확한 전송을 보장)

### UDP
데이터 전송을 보장하지 않는 프로토콜
- 신뢰성보다 실시간 스트리밍과 같이 시간에 민감한 애플리케이션을 사용하는 경우, 단방향으로 다수의 단말과 통신해 응답을 받기 어려운 환경에 사용
- 소켓 대신 IP를 기반으로 데이터를 전송

### 차이
||TCP|UDP|
|--|--|--|
|연결방식|가상회선 패킷 교환 방식(연결형)|데이터그램방식(비연결형)|
|전송순서|보장|바뀔 수 있음|
|수신 여부 확인|확인|확인X|
|통신 방식|1:1|1:1 or 1:N or N:N|


<br>
<br>

데이터그램 방식 : 데이터 전송 전에 송/수진자 사이에 가상 회선이라 불리는 논리적 경로를 설정하지 않고, 패킷들이 각기 독립적으로 전송되는 방식

흐름제어 : 송신측과 수신측의 데이터 처리 속도 차이를 해결하기 위한 기법
수신자가 패킷을 지나치게 많이 받지 않도록 조절하는 것

혼잡제어 : 송신측의 데이터 전달과 네트워크의 데이터 처리 속도 차이를 해결하기 위한 기법
네트워크의 혼잡을 피하기 위해 송신측에서 데이터의 전송속도를 조절하는 것