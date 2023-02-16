# REST API

</br>

### API(Application Programming Interface) 란?

- API의 맥락에서 애플리케이션이라는 단어는 고유한 기능을 가진 모든 소프트웨어를 나타낸다
- 인터페이스는 두 애플리케이션 간의 서비스 계약이라고 할 수 있다.
- 이 계약은 요청과 응답을 사용하여 두 애플리케이션이 서로 통신하는 방법을 정의한다.
- API 문서에는 개발자가 이러한 요청과 응답을 구성하는 방법에 대한 정보가 들어 있다.

![https://b1694534.smushcdn.com/1694534/wp-content/uploads/2022/01/image-768x331.png?lossy=1&strip=1&webp=1](https://b1694534.smushcdn.com/1694534/wp-content/uploads/2022/01/image-768x331.png?lossy=1&strip=1&webp=1)

</br>

### REST 구성

- **자원(RESOURCE)** - URI
- **행위(Verb)** - HTTP METHOD
- **표현(Representations)**

</br>

### REST 특징

1. **Uniform-Interface**

> Uniform Interface는 URI로 지정한 리소스에 대한 조작을 통일되고 한정적인 인터페이스로 수행하는 아키텍처 스타일을 말한다
> 
- 자원들이 각각의 독릭적인 인터페이스를 가져야 함
    - 웹 페이지가 변경 되었을 때 웹 브라우저에 영향이 없어야 함

1. **Stateless**

> 작업을 위한 상태정보를 따로 저장하고 관리하지 않는다
> 
- 세션 정보나 쿠키 정보를 별도로 저장하고 관리하지 않음
    - API 서버는 요청만을 단순히 처리하면 되기에 서비스의 자유도가 높아짐
- 서버에서 불필요한 정보를 관리하지 않기에 구현이 단순해짐

1. **Cacheable**

> REST 는 HTTP 기존 웹표준을 그대로 사용함
> 
- HTTP 가 가진 캐싱 기능이 적용 가
- 캐싱된 데이터가 유효한지를 판단하기 위해 'Last-modifed'와 'Etag'를 씀

1. **Self-descriptiveness**

> REST API 메시지만 보고도 이를 쉽게 이해 할 수 있는 자체 표현 구조로 되어 있음
> 
- HTTP Header에 타입을 명시하고 각 메시지(자원)들은 MIME types에 맞춰 표현해야 함
- ex) `application/json`, `font/ttf`, `text/plain`, `text/csv`

1. **Client - Server 구조**

> REST 서버와 client 의 역할이 확실히 구분되어 있어, 개발해야 할 내용이 명확하고, 서로간 의존성이 줄어듬
> 
- REST 서버는 API 제공
- client 는 사용자 인증이나 컨텍스트(세션, 로그인 정보) 등을 직접 관리

1. **Layered System(계층 구조)**

> REST 서버는 다중 계층으로 구성될 수 있음
> 
- 보안, 로드 밸런싱, 암호화 계층을 추가해 구조상의 유연성을 둘 수 있음
- PROXY, 게이트웨이와 같은 네트워크 기반의 중간매체를 사용할 수 있게함

</br>

### REST API 디자인

1. URI 는 정보의 자원을 표현해야 한다
2. 자원에 대한 행위는 HTTP Method로 표현한다(GET, POST, PUT, DELETE)
3. 긴 URI 사용 시 가독성을 위해 하이픈 `-` 사용 (밑줄은 지양 `_` )
4. URI 경로에는 소문자 사용
5. URI 는 계층적 내용을 담기에 `/집/아파트/전세` 와 같은 구조가 적합함
6. 동사가 아닌 명사로 표기하는 것을 지향
7. 확장자는 표기하지 않음
