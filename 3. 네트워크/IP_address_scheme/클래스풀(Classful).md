# 클래스풀(Classful)
> IP 주소는 인터넷 주소로, 네트워크 주소와 호스트 주소로 나뉜다. 네트워크 주소는 호스트들을 모은 네트워크를 지칭하며, 호스트 주소는 호스트를 구분하기 위한 주소이다.
> ![https://velog.velcdn.com/images%2Fborab%2Fpost%2F691c6f99-9c9d-4987-bbf9-728f1385d934%2Fimage.png](https://velog.velcdn.com/images%2Fborab%2Fpost%2F691c6f99-9c9d-4987-bbf9-728f1385d934%2Fimage.png)

</br>

### 클래스 A

- 2^24 – 2 = 한 네트워크당 16,777,214 호스트 ID(약 1600만개)
- 네트워크 주소 범위는 1 ~ 126 로 시작 / 원래는 127.255.255.255까지 포함하지만
127.X는 루프백 주소이기 때문에 포함 x

</br>

### 클래스 B

- 2^16 – 2 = 한 네트워크당 65534 호스트 ID(6만 5천개)
- 네트워크 주소 범위 : 128 ~ 191 로 시작

</br>

### 클래스 C

- 2^8 – 2 = 한 네트워크당 254 호스트 ID
- 네트워크 주소 범위 : 192 ~ 223 로 시작

</br>

### -2 를 하는 이유

- 맨 앞자리는 네트워크 주소로 남겨두며 마지막 주소는 브로드캐스팅 주소로 남겨놓음

</br>

### 클래스 풀의 문제점

![http://www.tcpipguide.com/free/diagrams/ipclasslesssolution.png](http://www.tcpipguide.com/free/diagrams/ipclasslesssolution.png)

- 위와 같이 호스트 주소가 5000개가 필요한 상황에서 클래스C 는 IP가 부족하고, B는 IP가 너무 많아 낭비
