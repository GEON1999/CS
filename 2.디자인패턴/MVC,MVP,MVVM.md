### MVC 패턴

> MVC패턴은 모델(Model), 뷰(View), 컨트롤러(Controller)로 이루어진 디자인 패턴이다
> 

![https://3.bp.blogspot.com/-0h7lFDhI1Ng/XnDpa3Jd3nI/AAAAAAAAAL4/4NBUmZgLOWMcf-2Qt-L38ONy20T1514dgCK4BGAYYCw/s1600/%25EC%25BA%25A1%25EC%25B2%2598.PNG](https://3.bp.blogspot.com/-0h7lFDhI1Ng/XnDpa3Jd3nI/AAAAAAAAAL4/4NBUmZgLOWMcf-2Qt-L38ONy20T1514dgCK4BGAYYCw/s1600/%25EC%25BA%25A1%25EC%25B2%2598.PNG)

- 뷰
    - 뷰(view)는 inputbox, checkbox, textarea 등 사용자 인터페이스 요소를 나타냄
    - 모델의 정보를 따로 저장하지 않고, 변경이 일어나면 컨트롤러에 이를 전달함
- 모델
    - 모델(model)은 애플리케이션의 데이터인 데이터베이스, 상수, 변수 등을 뜻함
    - 뷰에서 데이터를 생성하거나 수정할 때 컨트롤러를 거쳐 모델이 생성 혹은 업데이트 됨
    - textarea 가 view 라면 그 안의 text 가 모델이라고 볼 수 있음
- 컨트롤러
    - 하나 이상의 모델과 하나 이상의 뷰를 잇는 다리 역할
    - 메인로직을담당하고 모델과 뷰의 생명주기 또한 관리함
    

</br> 

- 장점
    - 세 가지 역할로 구분하였기에 각각의 구성 요소에만 집중하여 개발 가능
    - 재사용과 확장성에서 용이함
- 단점
    - 어플리케이션이 복잡해질수록 모델과 뷰의 관계가 복잡해짐
    

### MVC, MVP, MVVM 패턴 차이

| 특징 | MVC 패턴 | MVP 패턴 | MVVM 패턴 |
| --- | --- | --- | --- |
| 관계 | 컨트롤러와 뷰는 1 : n | 프레젠터와 뷰는 1 : 1  | 뷰모델과 뷰 는 1 : n |
| 참 | 뷰는 컨트롤러를 참조 x | 뷰는 프레젠터를 참조 o | 뷰는 뷰모델을 참조 o |
