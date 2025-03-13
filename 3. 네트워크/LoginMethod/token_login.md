# 토큰 기반 인증 방식
# 토큰 기반 인증 방식

> 토큰은 사용자 인증을 위한 정보를 서명한 것 이다
> 

세션 기반 인증은 클라이언트의 상태를 서버에 저장하며 요청마다 유효한 세션인지 확인해야하는 반면, 토큰 기반의 인증 방법은 토큰에 사용자 인증을 위한 정보가 담겨 있기 때문에 **사용자 정보를 서버에 저장하지 않고**, 전달 받은 토큰의 서명과 데이터를 검증하는 것만으로 인증이 가능하다

</br>

### JWT(JSON Web Token)

> JWT는 현재 토큰 인증에서 가장 많이 사용되는 인터넷 표준이다.
> 

애플리케이션의 엑세스 토큰을 만드는 데 주로 사용되며, 데이터들이 JSON 형태로 작성된다. 데이터를 비밀키 또는 공개/개인 키로 서명해 사용하고, 이를 통해 JWT는 인가와 정보 교환을 위해 사용할 수 있게된다. 사용자에게 발급된 토큰으로 인가된 서버 리소스에 접근할 수 있으며, 키를 통해 송신자를 확인할 수 있고, 데이이터의 무결성도 확인 가능하다.

![https://www.okta.com/sites/default/files/styles/tinypng/public/media/image/2020-12/TokenBasedAuthentication.png?itok=zXMogDjG](https://www.okta.com/sites/default/files/styles/tinypng/public/media/image/2020-12/TokenBasedAuthentication.png?itok=zXMogDjG)

</br>

### JWT 의 구조

![https://supertokens.com/static/b0172cabbcd583dd4ed222bdb83fc51a/9af93/what-is-jwt.png](https://supertokens.com/static/b0172cabbcd583dd4ed222bdb83fc51a/9af93/what-is-jwt.png)

1. Header
    - 어떠한 방법의 서명 알고리즘을 사용할 것인가에 대한 정보
2. Payload
    - 토큰에 담을 데이터(토큰 발급자, 토큰 유효기간)
        - 이 데이터를 JWT 에서는 claim 이라고 부르며 registered claims, public claims, private claims 세 종류가 있다
3. Signature
    - 헤더와 페이로드를 서명한 값
        - 서버는 이 서명과 전달된 헤더, 페이로드를 같은 알고리즘으로 해시한 값이 동일한 것임을 확인하여 유효한 토큰인지 검사함

</br>

### 장점

1. 사용자 인증에 필요한 모든 정보는 토큰 자체에 포함하기 때문에 별도의 인증
저장소가 필요 없습니다.
2. 다른 유형의 토큰과 비교했을 때 경량화되어있습니다. SAML(Security Assertion
Markup Language Tokens)이란 토큰이 있지만 이에 비해 훨씬 경량화되어있음.
3. 디코딩했을 때 JSON이 나오기 때문에 JSON을 기반으로 쉽게 직렬화, 역직렬화가
가능하다.

</br>

### 단점

1. 토큰이 비대해질 경우 서버과부화에 영향을 줄 수 있음
2. 토큰이 노출되는 순간 중요 정보들이 쉽게 노출됨
    - JWT의 페이로드에는 클라이언트와 서버가 사용할 데이터를 저장함
    - 이 데이터는 암호화되지 않고 base64로 인코딩한 값임
    - base64로 인코딩된 값은 누구나 디코딩해 데이터를 확인할 수 있음
    - 결론 : 페이로드에는 중요 정보, 민감 정보를 포함해서는 안됨
