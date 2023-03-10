# API 
>  Application Programming Interface
> 
- 둘 이상의 컴퓨터 프로그램이 서로 통신하는 방법이자 컴퓨터 사이에 있는 중계 계층
    - A 가 B 에게 요청한다고 했을 때, 어떻게 통신할 것인지, 어떤 데이터를 주고 받을 것인지 Method 는 무엇인지 등의 방법이 정의된 중계층

![Untitled](https://assets.website-files.com/5ff66329429d880392f6cba2/61544d5e45a2fb1285b5af5e_how%20api%20works.svg)

## API 의 장점

- 제공자는 서비스의 DB, 설계 구조 등을 드러내지 않고 사용자에게 원하는 것만 노출시킬 수 있음
- 사용자는 해당 서비스의 구현 방식 등의 불필요한 정보 없이 필요한 정보만을 받을 수 있음
- OPEN API 를 통해 앱 개발 시 필요로한 시간과 비용을 절약할 수 있음
    - OAuth 나 지도 어플의 연계를 통해 직접 지도를 구현하지 않고도 해당 작업을 수행할 수 있음
- 제공자의 경우 내부 DB 등의 프로세스가 수정되어도 API 를 선택적으로 업데이트할 수 있음(내부만 변경하고 API 는 수정하지 않을 수도 있음)
- 제공자는 API 를 통해 특정 이벤트가 발생했을 때의 데이터를 한곳에 모을 수 있음
- OPEN API 제공자의 경우 API 를 통해 데이터를 수집할 수도 해당 서비를 확장할 수도 있음
    - 파파고와 같은 인공지능 번역 시스템은 많은 양의 input 을 토대로 번역의 질이 향상 되는데, OPEN API 를 통해 이 input 의 양을 늘릴 수 있음

## API 의 종류

- private
    - 내부적으로 해시키를 통해 서버간 통신이 이루어짐 (해시키를 공유하여 통신)
- public
    - 모든 사람이 사용할 수 있음
    - 많은 트래픽을 방지하기 위해 제한을 두고 관리함
