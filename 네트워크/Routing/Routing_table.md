# 라우팅 테이블
> 라우팅 테이블은 IP 주소를 기반으로 라우터의 위치를 저장한 테이블 또는 데이터베이스
이며 다양한 네트워크에 대한 정보와 해당 네트워크에 연결하는 방법이 포함되어 있다.
> 

![https://t1.daumcdn.net/cfile/tistory/996A07375A39AFDE18?original](https://t1.daumcdn.net/cfile/tistory/996A07375A39AFDE18?original)

</br>

### 라우팅 테이블의 구성요소

- 네트워크 대상(Network Destination) : 목적지 네트워크의 IP 주소
- 서브넷 마스크(Netmask) : 대상 주소를 설명할 때 쓰이는 값
- 게이트웨이(Gateway): 이 장치와 연결되어있는 홉, 패킷이 전달되는 다음 IP 주소(외부 네트워크와 연결된 장치) 만약 목적지가 로컬 네트워크라면 “연결됨(connected)”라고 표기 되며 다른 네트워크라면 해당 네트워크의 게이트웨이를 가르킴
- 인터페이스(interface): 게이트웨이로 가기위해 거치는 장치 / 10.0.0.2는 eth3을 통해 접근이 가능
- 메트릭(Metric): 우선순위라고도 불리며 패킷 전송을 위해 최적의 경로가 선택되도록 참고되는 값. 동일한 라우팅테이블 요소가 2개 있을 때 이 값이 낮은 요소가 선택된다. 메트릭은 일반적으로 홉 수(hop count)가 들어가며 지연시간, 처리량 등이 들어갈 수 있음

```
게이트웨이(Gateway) : 게이트웨이는 프로토콜 변환기라고도 하며 네트워크와 네트워크를 잇는 장치다. 
라우터와 하는 기능차제가 비슷함

홉(Hop) : 홉(hop)은 네트워크에서 출발지와 목적지 사이에 위치한 장치를 의미하며 
홉 카운트(hopcount)는 데이터가 출발지와 목적지 사이에서 통과해야 하는 홉의 개수를 의미함
```

![https://blog.kakaocdn.net/dn/c1weeP/btqDahDuXh2/fcymOyyFb2FwiqZtVJnac1/img.png](https://blog.kakaocdn.net/dn/c1weeP/btqDahDuXh2/fcymOyyFb2FwiqZtVJnac1/img.png)
