[toc]

# 210226

## 새로 배운내용

### GNN 기초

#### 정점 표현 학습 복습

##### 정점 표현 학습

![image-20210226113647101](images/image-20210226113647101.png)

![image-20210226113657066](images/image-20210226113657066.png)

![image-20210226113707668](images/image-20210226113707668.png)

##### 변환식 정점 표현 학습과 귀납식 정점 표현 학습

![image-20210226113716817](images/image-20210226113716817.png)

![image-20210226113730909](images/image-20210226113730909.png)

![image-20210226113807599](images/image-20210226113807599.png)

#### 그래프 신경망 기본

##### 그래프 신경망의 구조

![image-20210226114307477](images/image-20210226114307477.png)![image-20210226114327659](images/image-20210226114327659.png)

![image-20210226114427893](images/image-20210226114427893.png)![image-20210226114443158](images/image-20210226114443158.png)![image-20210226114450664](images/image-20210226114450664.png)

층 별 집계 함수를 공유하는데, 층별로 받는 입력의 수가 다를 수 있다.

이것을 해결하기 위해 층별 집계 함수는 이웃들 정보의 평균을 구해서 신경망에 적용한다.[궁금한점](#그래프 신경망의 집계함수에서 평균말고 다른 함수를 적용하면 어떻게 될까?)

![image-20210226114458311](images/image-20210226114458311.png)![image-20210226114507218](images/image-20210226114507218.png)

![image-20210226114514526](images/image-20210226114514526.png)

![image-20210226114520247](images/image-20210226114520247.png)

##### 그래프 신경망의 학습

![image-20210226120058237](images/image-20210226120058237.png)

![image-20210226120107443](images/image-20210226120107443.png)

![image-20210226120114988](images/image-20210226120114988.png)

![image-20210226120122457](images/image-20210226120122457.png)

![image-20210226120132169](images/image-20210226120132169.png)

![image-20210226120141101](images/image-20210226120141101.png)

![image-20210226120150553](images/image-20210226120150553.png)

![image-20210226120156158](images/image-20210226120156158.png)

##### 그래프 신경망의 활용

![image-20210226120336992](images/image-20210226120336992.png)

![image-20210226120344936](images/image-20210226120344936.png)

![image-20210226120351690](images/image-20210226120351690.png)

#### 그래프 신경망 변형

##### 그래프 합성곱 신경망

![image-20210226120544089](images/image-20210226120544089.png)

![image-20210226120551514](images/image-20210226120551514.png)

![image-20210226120559620](images/image-20210226120559620.png)

##### GraphSAGE

![image-20210226120606264](images/image-20210226120606264.png)

![image-20210226120611949](images/image-20210226120611949.png)

#### 합성곱 신경망과의 비교

##### 합성곱 신경망과 그래프 신경망의 유사성

![image-20210226120622071](images/image-20210226120622071.png)

![image-20210226120627309](images/image-20210226120627309.png)

![image-20210226120632922](images/image-20210226120632922.png)

##### 합성곱 신경망과 그래프 신경망의 차이

#### 실습: DGL 라이브러리와 GraphSAGE를 이용한 정점 분류

##### 데이터 불러오기

![image-20210226121930011](images/image-20210226121930011.png)

![image-20210226121936259](images/image-20210226121936259.png)

##### GraphSAGE 정의

![image-20210226121943650](images/image-20210226121943650.png)

![image-20210226121948134](images/image-20210226121948134.png)

##### GraphSAGE 학습

![image-20210226121959569](images/image-20210226121959569.png)

##### GraphSAGE 평가

![image-20210226122005791](images/image-20210226122005791.png)

![image-20210226122012548](images/image-20210226122012548.png)

#### 9강 정리

![image-20210226122020568](images/image-20210226122020568.png)

### GNN 심화

#### 그래프 신경망에서의 어텐션

##### 기본 그래프 신경망의 한계

![image-20210226134400108](images/image-20210226134400108.png)

##### 그래프 어텐션 신경망

![image-20210226134407149](images/image-20210226134407149.png)

![image-20210226134416815](images/image-20210226134416815.png)

![image-20210226134425182](images/image-20210226134425182.png)

![image-20210226134432452](images/image-20210226134432452.png)

#### 그래프 표현 학습과 그래프 풀링

##### 그래프 표현 학습

정점을 벡터로 표현하는 것이 아니라 그래프를 벡터로 표현하는 것이다.

![image-20210226134814665](images/image-20210226134814665.png)

##### 그래프 풀링

[궁금한점](#미분가능한 풀링은 뭘까?)

![image-20210226134830205](images/image-20210226134830205.png)

#### 지나친 획일화 문제

##### 지나친 획일화 문제

그래프 신경망의 층의 수가 증가하면 많은 정점의 정보를 취합하는 과정에서 대부분의 정점이 겹치게 된다.

![image-20210226134854556](images/image-20210226134854556.png)

![image-20210226134910526](images/image-20210226134910526.png)

##### 지나친 획일화 문제에 대한 대응

![image-20210226134932674](images/image-20210226134932674.png)

![image-20210226134942218](images/image-20210226134942218.png)

#### 그래프 데이터 증강

##### 그래프 데이터 증강

![image-20210226135514332](images/image-20210226135514332.png)

##### 그래프 데이터 증강에 따른 효과

![image-20210226135521327](images/image-20210226135521327.png)

#### 실습: GraphSAGE의 집계 함수 구현

##### 데이터 불러오기

![image-20210226135606888](images/image-20210226135606888.png)

![image-20210226135622732](images/image-20210226135622732.png)

##### GraphSAGE 구현

![image-20210226135629323](images/image-20210226135629323.png)

![image-20210226135645404](images/image-20210226135645404.png)

![image-20210226135703788](images/image-20210226135703788.png)

![image-20210226135752716](images/image-20210226135752716.png)

![image-20210226135800229](images/image-20210226135800229.png)

##### GraphSAGE 학습

![image-20210226135807549](images/image-20210226135807549.png)

##### GraphSAGE 평가

![image-20210226135815638](images/image-20210226135815638.png)

![image-20210226135823268](images/image-20210226135823268.png)

#### 10강 정리

![image-20210226135835709](images/image-20210226135835709.png)

## 참고용

![image-20210226140713548](images/image-20210226140713548.png)

![image-20210226140721677](images/image-20210226140721677.png)

[Semi-Supervised Classification with Graph Convolutional Networks](https://arxiv.org/abs/1609.02907) 

[A Comprehensive Survey on Graph Neural Networks](https://arxiv.org/pdf/1901.00596.pdf)

## 궁금한 점

### 그래프 신경망의 집계함수에서 평균말고 다른 함수를 적용하면 어떻게 될까?

[돌아가기](#그래프 신경망의 구조)

GraphSAGE를 참고하면 되겠다.

[GraphSAGE](#GraphSAGE)

### 그래프 합성곱 신경망에서 정규화 방법이 바뀐게 어떤 의미를 가질까?

이웃의 정보를 취합할때, 이웃의 이웃의 갯수를 고려해준다는 의미인가?

### 미분가능한 풀링은 뭘까?

