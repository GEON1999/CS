# 전략 패턴
> 객체의 행위를 동적으로 바꾸고 싶은 경우, 컨텍스트 안의 전략만을 바꾸어 사용이 가능한 패턴
> 

![https://t1.daumcdn.net/cfile/tistory/9916204B5BF8DAD105?original](https://t1.daumcdn.net/cfile/tistory/9916204B5BF8DAD105?original)

- move 라는 컨텍스트 안의 train 혹은 bus 라는 캡슐화된 전략을 선택해서 사용 가능
    - `client.move.tarin()` 혹은 `client.move.bus()`
- 실제 사용 예시로는 **로그인 수단** 혹은 **결제 수단** 등이 있음
