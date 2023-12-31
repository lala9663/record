네트워크에서 통신이 일어나는 과정을 7단계로 나눈 것을 말한다.

![[Pasted image 20231025000751.png]]

1계층 - 물리계층
- 주로 전기적, 기계적, 기능적인 특성을 이용해서 통신 케이블로 데이터를 전송하게 된다.
- 케이블, 리피터, 허브를 통해 데이터를 전송한다.

2계층 - 데이터 링크 계층
- 물리계층을 통해 송수신되는 정보의 오류와 흐름을 관리하여 안전한 정보의 전달을 수행할 수 있도록 도와준다.
- 브리지, 스위치 등

3계층 - 네트워크 계층
- 데이터를 목적지까지 가장 안전하고 빠르게 전달하는 기능(라우팅)
- 주소부여(IP), 경로설정(Route)

4계층 - 전송 계층
- 통신을 활성화하기 위한 계층
- 보통 TCP프로토콜을 이용하며, 포트를 열어서 응용프로그램들이 전송을 할 수 있게 한다.
- 패킷 생성 및 전송

5계층 - 세션 계층
- 데이터가 통신하기 위한 논리적인 연결

6계층 - 표현 계층
- 데이터 표현이 상이한 응용 프로세스의 독립성을 제공하고, 암호화 한다.
- 사용자의 명령어를 완성 및 결과 표현. 포장/압축/암호화

7계층 - 응용 계층
- 최종 목적지로서 HTTP, SMTP 등과 같은 프로토콜이 있다.
- 네트워크 소프트웨어 UI 부분, 사용자의 입출력(I/O)부