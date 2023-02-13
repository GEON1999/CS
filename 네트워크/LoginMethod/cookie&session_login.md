# 세션 기반 인증 방식
![https://hudi.blog/static/b5affd77fa3033fe93b4c3c0b438fc25/3e3fe/session.png](https://hudi.blog/static/b5affd77fa3033fe93b4c3c0b438fc25/3e3fe/session.png)

1. 클라이언트에서 로그인 시도(post request)
2. 서버에서 session id를 만들고 해당 id 를 cookie 에 담아 클라이언트에 return 하고 DB에도 저장
3. 클라이언트에서 서버로 요청을 보낼 때 마다 session id 를 담은 cookie 를 담아 보냄으로서 로그인 상태임을 인증

</br>

### 단점

1. 사용자의 상태에 관한 데이터를 서버에 저장했을 때 로그인 중인 유저의 수가 늘어난다면 서버의 메모리 과부화가 일어날 수 있음
2. DB 중 RDBMS에 저장한다면 직렬화 및 역직렬화에 관한 오버헤드가 발생함

</br>

**세션 기반 로그인 방식을 사용한 프로젝트**

[당근마켓 클론 github](https://github.com/GEON1999/carrot-market)
