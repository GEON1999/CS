# 네트워크 토폴로지#2
### 토폴로지의 필요성
> 토폴로지는 병목현상을 해결하는 척도가 된다
- 병목현상(bottleneck) : 병목 현상은 트래픽에 의해 데이터 흐름이 제한되는 상황을 말함(핫스팟)

![https://t1.daumcdn.net/cfile/tistory/997C87485DC5329201](https://t1.daumcdn.net/cfile/tistory/997C87485DC5329201)

</br>

## 링형 토폴로지

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F254385505668EC8E06](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F254385505668EC8E06)

- 고리 형태
- 노드 추가, 삭제가 용이함

### 장점

- 노드 수가 많아져도 데이터 손실이 없음

### 단점

- 링크 또는 노드 하나에 장애 발생 시 전체 네트워크에 영향을 끼침
- 토큰이 없는 노드는 통신에 참여를 못하며 데이터 공유가 안됨

</br>


## 메시 토폴로지

![https://thebook.io/img/080326/073.jpg](https://thebook.io/img/080326/073.jpg)

- 그물망 형태
- 노드 추가 및 삭제가 어려움

### 장점

- 안정성이 높음
    - 특정 노드의 장애가 다른 노드에 영향을 주지 않음
- 트래픽 분산이 가능

### 단점

- 회선이 비효율적으로 많기에, 구축 비용이 비
