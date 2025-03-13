# 쿠키(Cookie)
> 웹 브라우저에 저장되는 작은 텍스트 파일로, 사용자의 웹 환경을 기억하고, 접속 정보를 저장하거나 불러오는 기술을 제공함
> 

![http://taeyo.net/columns/images/webapi-cookies01.png](http://taeyo.net/columns/images/webapi-cookies01.png)

- 클라이언트가 서버에 요청을 하면 서버는 응답 시 쿠키에 저장하고자하는 정보를 응답헤더의 Set-Cookie 로 전달함
- 클라이언트에서 요청헤더에 Cookie 를 설정하고 자동으로 서버에 전달되게 함
- 클라이언트에서 쿠키를 설정하고 보낼 수도 있지만, 보안상 클라이언트의 보안보다 서버의 보안이 강함으로 권장되지 않음
- Expires 또는 Max-Age 속성을 지정하지 않으면 브라우저가 종료되면서 쿠키도 사라짐
    - 속성을 지정하면 특정 날짜 또는 일정 기간이 지나면 삭제됨
