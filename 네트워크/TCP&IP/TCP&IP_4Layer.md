# TCP/IP 4계층
> 장치들이 인터넷 상에서 데이터를 주고받을 때 쓰는 독립적인 프로토콜의 집합을 의미함
> 
- TCP(Transmission Control Protocol)
- IP(Internet Protocol)
- 인터넷을 통해 데이터를 보낼 때 주로 TCP 와 IP 를 이용해서 보내기 때문에 이런 용어를 가짐

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F213F623C566BAE253B](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F213F623C566BAE253B)

</br>

### 애플리케이션 계층

> HTTP, SMTP, SSH, FTP가 대표적이며 웹 서비스, 이메일 등 서비스를 실질적으로
사람들에게 제공하는 층

</br>

### 전송 계층

> TCP, UDP가 대표적이며 애플리케이션계층에서 받은 메시지를 기반으로 세그먼트 또는
데이터그램으로 데이터를 쪼개고 데이터가 **오류**없이 순서대로 전달되도록 도움을 주는
층


</br>

### 인터넷 계층

> IP, ICMP, ARP가 대표적이며 한 노드에서 다른 노드로 전송 계층에서 받은 세그먼트 또는
데이터그램을 패킷화 하여 목적지로 전송하는 역할
> 

</br>

### 링크 계층

> 링크 계층은 전선, 광섬유, 무선 등으로 데이터가 네트워크를 통해 물리적으로 전송되는
방식을 정의
> 

</br>

### 캡슐화와 비캡슐화

> 네트워크에서 캡슐화(encapsulation)란 송신자가 수신자에게 데이터를 보낼 때 데이터가 각
계층을 지나며 각 계층의 특징들이 담긴 헤더들이 붙여지는 과정을 의미
> 

![https://t1.daumcdn.net/cfile/tistory/99803C415BA2F07C06?original](https://t1.daumcdn.net/cfile/tistory/99803C415BA2F07C06?original)

> 비캡슐화(decapsulation)란 이 과정의 역과정입니다. 수신자측에서는 이렇게 캡슐화된
데이터를 역순으로 제거하면서 응용계층까지 도달하는 것
> 

</br>

### PDU

> PDU(protocol data unit)란 TCP/IP 4계층을 기반으로 설명했을 때 각 계층의 데이터
단위를 의미
> 
- 애플리케이션 계층: 메시지
- 전송 계층: 세그먼트(TCP), 데이터그램(UDP)
- 인터넷 계층: 패킷
- 링크 계층: 프레임(데이터 링크 계층), 비트(물리 계층)
- 세그먼트 : 적절한 크기로 쪼갠 조각 (세그먼트와 데이터그램의 의미는 같음)
- 패킷 : 세그먼트에 SP와 DP가 포함된 IP 헤더가 붙은 형태의 조각
- 프레임 : MAC주소 헤더와 CRC/체크섬 트레일러가 붙은 조각
