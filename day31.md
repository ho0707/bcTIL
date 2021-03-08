[toc]

# 210308

## 새로 배운내용

### Image classification

#### Course overview

시각을 통해 받아들인 정보를 해석하는 것은 지능의 중요한 영역이다.

![image-20210308190236365](images/image-20210308190236365.png)

![image-20210308190324138](images/image-20210308190324138.png)

![image-20210308190425761](images/image-20210308190425761.png)

![image-20210308190451509](images/image-20210308190451509.png)

![image-20210308190513388](images/image-20210308190513388.png)

![image-20210308190627125](images/image-20210308190627125.png)

![image-20210308190646323](images/image-20210308190646323.png)

사람이 feature를 뽑아내는 것보다 딥러닝이 잘 되는 이유는 사람이 찾지 못한 feature를 찾아낼 수 도 있고, 사람이 찾아낸 feature를 제대로 모델링하지 못할 수도 있기때문이다.

#### Image classification

![image-20210308190906967](images/image-20210308190906967.png)

![image-20210308191001601](images/image-20210308191001601.png)

![image-20210308191023242](images/image-20210308191023242.png)

fc layer가 잘 동작하지 않는 이유는 영역의 정보를 저장하지 않기 때문인 것 같다.

![image-20210308191211463](images/image-20210308191211463.png)

![image-20210308191308512](images/image-20210308191308512.png)

#### CNN architectures for image classification 1

![image-20210308191459975](images/image-20210308191459975.png)

### Annotation data efficient learning

#### Data augmentation

사람이 카메라로 찍은 사진은 편향이 생긴다.

![image-20210308194921095](images/image-20210308194921095.png)

![image-20210308195000876](images/image-20210308195000876.png)

![image-20210308195010519](images/image-20210308195010519.png)

![image-20210308195032984](images/image-20210308195032984.png)

![image-20210308195119950](images/image-20210308195119950.png)

![image-20210308195130962](images/image-20210308195130962.png)

![image-20210308195140171](images/image-20210308195140171.png)

![image-20210308195149922](images/image-20210308195149922.png)

![image-20210308195200333](images/image-20210308195200333.png)

![image-20210308195208381](images/image-20210308195208381.png)

![image-20210308195217208](images/image-20210308195217208.png)

![image-20210308195228602](images/image-20210308195228602.png)

![image-20210308195236561](images/image-20210308195236561.png)

![image-20210308195245223](images/image-20210308195245223.png)

![image-20210308195255650](images/image-20210308195255650.png)

![image-20210308195353433](images/image-20210308195353433.png)

#### Leveraging pre-trained information

![image-20210308195416720](images/image-20210308195416720.png)

![image-20210308195432237](images/image-20210308195432237.png)

![image-20210308195444897](images/image-20210308195444897.png)

![image-20210308195454815](images/image-20210308195454815.png)

![image-20210308195515657](images/image-20210308195515657.png)

![image-20210308195528212](images/image-20210308195528212.png)

![image-20210308195537142](images/image-20210308195537142.png)

![image-20210308195547637](images/image-20210308195547637.png)

![image-20210308195559927](images/image-20210308195559927.png)

![image-20210308195607594](images/image-20210308195607594.png)

![image-20210308195622551](images/image-20210308195622551.png)



#### Leveraging unlabeled dataset for training

## 참고용

[VGGNet](https://arxiv.org/pdf/1409.1556.pdf)

[CutMix](https://arxiv.org/pdf/1905.04899.pdf)

## 궁금한 점

