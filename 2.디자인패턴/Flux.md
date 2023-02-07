# FLUX 패턴
![https://blog.kakaocdn.net/dn/ALrHe/btqBTMSuHfN/ZlW9i9ET34e90APgCRChk1/img.png](https://blog.kakaocdn.net/dn/ALrHe/btqBTMSuHfN/ZlW9i9ET34e90APgCRChk1/img.png)

- MVC 는 양방향 데이터 흐름을 가지고 있는데, 이로인해 데이터가 커지면 복잡해짐

![https://blog.kakaocdn.net/dn/lmfPW/btqBQnTPgIs/Z1jmHHdNcOTNiu93kQ9gMk/img.png](https://blog.kakaocdn.net/dn/lmfPW/btqBQnTPgIs/Z1jmHHdNcOTNiu93kQ9gMk/img.png)

- 페이스북에서는 메세지 알람등의 효율화를 위해 단방향 데이터 흐름인 FLUX 를 만듬
    - 페이스북 메세지가 수신되면 알림이 여러 view 에서 알림이 표시되어야 하고, 메시지 확인 시 표시되는 알림이 모두 사라져야함
    - 위와 같은 일련의 과정에서 데이터가 중첩되고 복잡해지며 버그 발생 시 원인이 파악이 힘들어져, 단방향 데이터 흐름인 flux 를 만듬
    

## Dispatcher

Dispatcher는 Flux의 모든 데이터 흐름을 관리하는 허브 역할을 하는 부분입니다. Action이 발생되면 Dispatcher로 전달되는데, Dispatcher는 전달된 Action을 보고, 등록된 콜백 함수를 실행하여 Store에 데이터를 전달합니다. Dispatcher는 전체 어플리케이션에서 한 개의 인스턴스만 사용됩니다.

## Store

어플리케이션의 모든 상태 변경은 Store에 의해 결정이 됩니다. Dispatcher로 부터 메시지를 수신 받기 위해서는 Dispatcher에 콜백 함수를 등록해야 합니다. Store가 변경되면 View에 변경되었다는 사실을 알려주게 됩니다. Store은 [싱글톤](https://ko.wikipedia.org/wiki/%EC%8B%B1%EA%B8%80%ED%84%B4_%ED%8C%A8%ED%84%B4)으로 관리됩니다.

## View

Flux의 View는 화면에 나타내는 것 뿐만이나라, 자식 View로 데이터를 흘려 보내는 뷰 컨트롤러의 역할도 함께 합니다.

## Action

Dispatcher에서 콜백 함수가 실행 되면 Store가 업데이트 되게 되는데, 이 콜백 함수를 실행 할 떼 데이터가 담겨 있는 객체가 인수로 전달 되어야 합니다. 이 전달 되는 객체를 Action이라고 하는데, Action은 대채로 액션 생성자(Action creator)에서 만들어집니다.
