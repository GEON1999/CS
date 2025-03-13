# 4Way-Handshake
1. 먼저 클라이언트가 연결을 닫으려고 할 때 FIN으로 설정된 세그먼트를 보냄. 그리고 클라이언트는 FIN_WAIT_1 상태로 들어가고 서버의 응답을 기다림.
2. 서버는 클라이언트로 ACK라는 승인 세그먼트를 보내고 CLOSE_WAIT 상태에 들어감. 클라이언트가 세그먼트를 받으면 FIN_WAIT_2 상태에 들어감.
3. 서버는 LAST_ACK상태가 되며 일정 시간 이후에 클라이언트에 FIN이라는세그먼트를 보냄
4. 클라이언트는 TIME_WAIT 상태가 되고 다시 서버로 ACK를 보내서 서버는 CLOSED 상태가 되며 이후 클라이언트는 어느 정도의 시간(TIME_WAIT으로 설정된 시간)을 대기한 후 연결이 닫힘

![https://t1.daumcdn.net/cfile/tistory/99229C485C1D90C038?original](https://t1.daumcdn.net/cfile/tistory/99229C485C1D90C038?original)

</br>

### TIME_WAIT

- 지연 패킷이 발생했을 때 데이터 무결성을 해결하기 위함
- 연결을 올바르게 닫힌상태로 만들기 위해 존재

```
TIME WAIT 은 MSL의 두배 시간을 기다림
- MSL 은 OS 마다 상이함(unbuntu : 60s, window : 4min)
```
