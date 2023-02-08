# 3Way-Handshake
1. SYN 단계: 클라이언트는 서버에 클라이언트의 ISN을 담아 SYN을 보냄.
2. SYN + ACK 단계: 서버는 클라이언트의 SYN을 수신하고 서버의 ISN을 보내며
승인번호로 클라이언트의 ISN + 1을 보냄
3. ACK 단계: 클라이언트는 서버의 ISN + 1한 값인 승인번호를 담아 ACK를 서버에
보냄

```jsx
SYN : synchronization의 약자, 연결 요청 플래그
ACK : acknowledgement의 약자, 응답 플래그
```

![https://imagedelivery.net/xE6X7mlbIExkQau-XHoj-A/f29c9e8a-4f2a-44ef-2682-8e49cf671d00/public](https://imagedelivery.net/xE6X7mlbIExkQau-XHoj-A/f29c9e8a-4f2a-44ef-2682-8e49cf671d00/public)

</br>

### ISN

> ISN : TCP(Transmission Control Protocol) 기반 데이터 통신에서 각각의 새 연결에 할당된
고유한 32비트 시퀀스 번호를 나타
> 
- TCP 연결을 통해 전송되는 다른 데이터 바이트와 충돌하지 않는 시퀀스 번호를 할당하는 데 도움이 됨

</br>

### 클라이언트와 서버의 상태

![https://velog.velcdn.com/post-images/jjewqm/df122a70-0ec4-11ea-a710-73066240b450/3-way.png](https://velog.velcdn.com/post-images/jjewqm/df122a70-0ec4-11ea-a710-73066240b450/3-way.png)

위와 같은 과정을 TCP 는 거치기에 신뢰성이 있고, UDP 는 신뢰성이 없다고 말할 수 있
