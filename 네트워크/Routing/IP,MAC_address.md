## IP 주소

- IP는 컴퓨터의 주소가 아니라 LAN card에 연결되어 있는 회선(랜선)의 주소를 뜻함
- 논리적 주소이며 인터넷망에 접속할 때 마다 달라짐

</br>

## MAC 주소

- MAC 주소는 LAN card의 주소를 뜻함
- 네트워크 상에서 서로를 구분하기 위해 device 마다 할당된 물리적인 주소 (별도 조작없이는 고정되어 있음)
- 48비트로 이루어져있으며, 24비트의 OUI 와 24비트의 UAA 로 이루어져있음
    - OUI : IEEE에서 할당한 제조사 코드
    - UAA : 제조사에서 구별되는 코드
    
</br>

### IP&MAC 주소를 쓰는 이유

> IP는 최적의 경롤르 찾아주는 라우팅을 위한 주소이고, 실질적인 통신은 MAC 주소로 한다.
> 
- 라우팅 기법은 패킷에 포함된 IP 주소를 추적해서 최단 경로를 찾아감
- IP 에서 IP 주소로 목표된 네트워크로 패킷을 보냄
- 그곳에서 IP에 등록된 MAC 주소로 변환되어 컴퓨터로 패킷을 전송한다

</br>

### ARP & RARP

> ARP를 통해 논리적 주소인 IP 주소를 물리적 주소 MAC 주소로 변환함(RARP는 반대)
> 

![https://blog.kakaocdn.net/dn/b11fw1/btqBUS6ug9V/3KFThmyYxf9pjKqtgYSE7k/img.png](https://blog.kakaocdn.net/dn/b11fw1/btqBUS6ug9V/3KFThmyYxf9pjKqtgYSE7k/img.png)

- ARP의 과정
    1. 해당 IP 주소에 맞는 MAC 주소를 찾기 위해 데이터를 **브로드캐스팅** 으로 연결된 네트워크에 있는 모든 장치한테 보냄
    2. 맞는 장치가 있다면 그림 **3** 번과 같이 request 를 보낸 장치에게 유니캐스트로 테이터를 전달해 주소를 찾게 됨
