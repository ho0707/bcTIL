[toc]

# 210310

## 새로 배운내용

### R-CNN vs Fast R-CNN vs Faster R-CNN

Fast R-CNN은 ROI마다 Feature map을 다시 계산하지 않아서 속도가 빠르다

Faster R-CNN은 Resion proposal이 아니라 RPN을 이용해서 신경망으로 학습해 ROI를 찾아낸다. (Anchor Box)

![image-20210310152700105](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310152700105.png)

### One-stage vs Two-stage

One stage는 ROI가 없다.

![image-20210310173359546](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310173359546.png)

### Focal loss

 CE의 확장판으로 값을 낮게 측정했을때 더 가파르게 학습한다. (기울기)

![image-20210310173303001](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310173303001.png)

## 참고용

### t-SNE

### Non-Maximum Suppression

### SCOUTER

### RetinaNet

### DETR



![image-20210310165710253](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310165710253.png)

![image-20210310165718473](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310165718473.png)

![image-20210310165659278](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310165659278.png)

## 궁금한 점

### CAM은 왜 ReLU를 안쓸까?

아래 그림들을 보면 CAM에서는 모든 값이 음수가 나올 수 있다.

Grad-CAM은 ReLU를 통과하기전에 값이 클래스가 yc로 분류될 확률에 기여한 값이기 때문에 모든 값이 음수라면 yc로 분류되지 않았을것이다.

![image-20210310165224189](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310165224189.png)

![image-20210310165301943](C:\Users\ho070\AppData\Roaming\Typora\typora-user-images\image-20210310165301943.png)