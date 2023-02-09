## IPv4

- 32비트, 2^32개의 주소(41억 9천만) 표현
- 8비트 단위로 점을 찍어 4개로 구분(옥텟)
- 8비트를 10진수로 표현
- 2^32개의 주소로는 부족하기에, NAT, 서브네팅 등의 부수적인 기술 필요

![https://www.freecodecamp.org/news/content/images/size/w1000/2021/03/1125px-Ipv4_address.png](https://www.freecodecamp.org/news/content/images/size/w1000/2021/03/1125px-Ipv4_address.png)

</br>

## IPv6

- 128비트, 2^ 128개의 주소 표현(많은 주소 처리가능하며 NAT, 서브네팅이 필요하지 않음)
- 16비트씩 8개로 구분
- 16비트는 16진수로 변환되어 콜론(:)으로 구분하여 표시
- 앞의 연속되는 0은 생략될 수 있음.

![http://www.steves-internet-guide.com/wp-content/uploads/ipv6-address-structure.jpg](http://www.steves-internet-guide.com/wp-content/uploads/ipv6-address-structure.jpg)

- 앞 64비트는 네트워크, 뒤 64비트는 인터페이스 주소로 구성되어 있음

</br>

### IPv4 vs IPv6

> 보안, 속도 측면서에서 보통은 IPv6가 우위에 있음
> 

![https://linux-console.net/common-images/ipv4-and-ipv6-comparison/ipv4-ipv6-620x349.gif](https://linux-console.net/common-images/ipv4-and-ipv6-comparison/ipv4-ipv6-620x349.gif)

- IPv6 에는 체크섬(CRC)이 없다
    - 상위 프로토콜인 TCP, UDP(선택) 에 이미 체크섬이 있기 때문임
- IPv6 에는 IPSec이 내장되어 있음
    - 데이터 패킷을 암호화 하는 보안 네트워크 프로토콜 제품군
- IPv6 는 IPv4 의 불필요한 헤드 필드를 제거하여 보다 빠른 처리 가능
- IPv4는 헤더가 가변길이지만, IPv6는 40바이트로 고정길이임
