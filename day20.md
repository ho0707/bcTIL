[toc]

# 210219

## 새로 배운내용

### 1.GPT-1

special token을 통해 다양한 task를 처리할 수 있는 통합된 모델을 제안했다.

Classification

Extract token의 인코딩 벡터를 Output layer에 입력해 예측한다.

Entailment

문장을 구별하기 위해 Delimeter token을 추가하고

Extract token의 인코딩 벡터를  Output layer에 입력해 예측한다.

![image-20210219150141128](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210219150141128.png)

fine tunning을 할때는 output layer를 떼어내고

encoding vector만을 받아서 사용하기 위해 추가적인 레이어를 붙여서 학습시킨다.

이때 transformer layer는 학습율을 낮게잡아서 큰 변화가 일어나지 않도록 한다.

## 참고용



## 궁금한 점

