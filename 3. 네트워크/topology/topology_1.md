# 네트워크 토폴로지
> 네트워크 토폴로지란 노드와 링크가 어떻게 구성되어 있는지를 의미함
> 

## 버스

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F277F67505668EC8B37](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F277F67505668EC8B37)

- 메인 회선에 여러개의 노드가 연결되는 형태
- 노드 추가 및 삭제가 용이함

### 장점

- 소규모 네트워크 구축이 쉬움
    - 설치 비용이 적음
- 특정 노드에 장애가 발생하더라도 다른 노드에 영향 없음

단점

- 메인 링크에 많은 트래픽 발생 시 정체현상 발생 가능성 높음
- 메인 링크에 장애가 있을 경우 리스크가 큼

## 스타 토폴로지

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2245E8505668EC8904](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2245E8505668EC8904)

- 중앙에 있는 노드를 중심으로 연결된 형태
- 노드 추가 및 삭제가 용이함

### 장점

- 중앙 노드 제외 특정 노드에 장애가 발생해도 다른 노드에 영향 없음
- 안정성이 높음
    - 중앙 노드 제외 특정 노드에 침해가 발생했을 경우, 다른 노드로의 확장이 어렵움
        - 다른 노드로 이동할 시 중앙 노드를 거쳐야 하는데, 통상적으로 중앙노드의 방화벽의 보안 상태가 높음
- 특정 링크에 문제가 생겨도 해당 링크에만 영향이 있음

### 단점

- 중앙 노드에 장애 발생 시 리스크가

## 트리 토폴로지

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2549FD505668EC8C01](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F2549FD505668EC8C01)

- 계층적 토폴로지
- 노두 추가, 삭제 난이도 보통
    - 리프노드 삭제 및 추가는 쉬움
    - 루트 노드 혹은 부모 노드 삭제 및 추가는 어려움
- 버스 토폴로지와 스타 토폴로지의 하이브리드 형태

### 장점

- 노드 확장에 용이함
- 리프 노드에서의 장애는 다른 곳에 영향을 끼치지 않음

### 단점

- 특정 노드 트래픽 집중 시 하위 노드에 영향 발생
- 루트 노드에 장애 발생 시 전체 네트워크에 영향 발
