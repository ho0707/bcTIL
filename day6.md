[toc]

# 210125

## 새로 배운내용

### 1.np.newaxis

![image-20210125132747033](images/image-20210125132747033.png)

### 2.무어-펜로즈 역행렬

![image-20210128103531798](images/image-20210128103531798.png)

![image-20210128103813190](images/image-20210128103813190.png)

## 참고용

### 1.np.array 사용시 dtype 필수로 적어줘야함

![image-20210125123314713](images/image-20210125123314713.png)

### 2.ndarray slicing

![image-20210125130849643](images/image-20210125130849643.png)



![image-20210125131046043](images/image-20210125131046043.png)

들어있는 값은 같지만 차원이 다르다.



스텝도 사용가능

![image-20210125131201574](images/image-20210125131201574.png)



### 3.np.arange

스텝으로 소수도 가능하다.

![image-20210125131250311](images/image-20210125131250311.png)

### 4.ones, zeros, empty

![image-20210125131441224](images/image-20210125131441224.png)

### 5.something_like(ones, zeros, empty)

![image-20210125131751793](images/image-20210125131751793.png)

### 6.idemtity, eye, diag

![image-20210125131818545](images/image-20210125131818545.png)

![image-20210125131846414](images/image-20210125131846414.png)

![image-20210125131910425](images/image-20210125131910425.png)

### 7.random sampling(uniform, normal)

![image-20210125132118369](images/image-20210125132118369.png)

### 8.axis

axis는 계산을 진행하는 축이다.

![image-20210125132335052](images/image-20210125132335052.png)

### 9.concatenate(vstack, hstack, axis)

![image-20210125132605611](images/image-20210125132605611.png)

![image-20210125132637343](images/image-20210125132637343.png)

### 10.dot product

np.array의 기본 연산은 같은위치의 연소끼리 연산이다.

dot product를 하려면 메소드를 사용

![image-20210125133024665](images/image-20210125133024665.png)

### 11.np.linalg.inv (역행렬)

![image-20210128103341393](images/image-20210128103341393.png)

## 궁금한 점

![image-20210128095200582](images/image-20210128095200582.png)

ln norm 에서 n은 양의 정수만 사용하나?

기계학습에서는 학습의 목적에 따라 다른 거리공간을 사용한다고 한다.

데이터의 특징을 고려해서 거리공간을 설계해야 하는듯 함

