## MTU

> MTU(Maximum Transmission Unit)란 네트워크에 연결된 장치가 받아들일 수 있는 최대
데이터 패킷의 크기를 뜻
> 
- 이크기를 기준으로 데이터는 쪼개져서 패킷화됨
- 네트워크 경로 상에 MTU 보다 큰 장치가 있으면 분할될 수도 있음

</br>

### 패킷이 분할되지 않는 경우

**IPv6**

- IPv6는 ****분할을 허용하지 않음

**IPv4**

- IPv4 헤더에는 flags라는 필드가 있는데 여기서 bit 이 1이되면 "Don't Fragment" 플래그가
활성화된다라는 의미이며, 이 때 분할이 불가능함

</br>

## MSS

> MSS(Maximum Segment Size)는 데이터의 크기만을 가르킴
> 

![https://blog.kakaocdn.net/dn/18T43/btrgBmg94PP/wXkcVUy9C0bwbXBj5HXLHk/img.png](https://blog.kakaocdn.net/dn/18T43/btrgBmg94PP/wXkcVUy9C0bwbXBj5HXLHk/img.png)

</br>

## PMTUD

> PMTUD(Path MTU Discovery)는 수신자와 송신자의 경로 상에서 장치가 패킷을 누락한
경우 테스트 패킷의 크기를 낮추면서 MTU에 맞게끔 반복해서 보내는 과정을 뜻
>
