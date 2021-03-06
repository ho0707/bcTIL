[toc]

# 210217

## 새로 배운내용

### 1.seq2seq

RNN, LSTM, GRU를 사용하는 경우에 문장 앞부분의 정보가 유실될 가능성이 크다. 번역의 경우 앞부분을 잘못 해석하는경우 전체 문장이 잘못될 가능성이 매우 크다.

여기서 문장을 거꾸로 입력하는 아이디어도 있다.(home go I)



![image-20210217101332317](images/image-20210217101332317.png)



#### attention

이런 문제를 해결할 수 있는 구조가 attention이다.

decoder에서 input과 hidden vector를 계산한 후 이 벡터를 encoder에서 계산한 hidden vector들과 내적을 통해 가중치를 계산한다.

그리고 가중평균(attention output)과 함께 다음 단어를 예측한다.

![image-20210217101908149](images/image-20210217101908149.png)

training단계에서 잘못 출력된 단어를 다음 입력으로 넣는것이 아니라 ground truth를 입력하는 것을 Teacher forcing이라 한다. 학습은 더 잘 진행되지만 실제 추론단계와는 다른 환경이기 때문에 둘을 적절히 섞어서 사용하는 방법도 있다.

![image-20210217102601990](images/image-20210217102601990.png)

##### attention score

attention score를 구하는 방법이 내적만 있는것이 아니다.

아래 식에서 내적은 general한 경우의 W벡터가 항등행렬인것과 같다.

W벡터는 학습가능한 행렬로 취급할 수 있다.

concat방식은 2개의 층을 쌓은것이다.(W, v)

![image-20210217103013234](images/image-20210217103013234.png)

##### summarize

![image-20210217103322867](images/image-20210217103322867.png)

### 2.Beam Search

attention 구조를 가진다 하더라도 Greedy decoding 문제를 겪는다.

중간에 한 단어가 잘못 생성되면 다시 돌아갈 수 없다.

![image-20210217113109055](images/image-20210217113109055.png)

P(y|x)를 최대화 하는것은 각각의  P(y1|x), P(y2|y1, x) 등을 최대화 하는것으로 보장되지 않는다. 

모든 경우를 따져보기에는 |V|^t 만큼의 계산을 해보아야 하므로 불가능하다.

![image-20210217113357129](images/image-20210217113357129.png)

Beam Search는 모든 경우를 다 따져보는것은 아니지만 k개의 가능한 단어들을 살펴보며 가장 큰 확률을 가지는 y를 선택한다. (k^t가 아니라 매 step마다 k개의 경우만 남긴다.)

계산의 편의를 위해 확률값에 로그를 취한다.

![image-20210217114227811](images/image-20210217114227811.png)

Beam Search의 경우 <EOS> 토큰이 서로 다른 시점에 나오므로 언제 Stop할지 정해야한다.

<EOS> 토큰이 나오면 임시 저장공간에 저장을 해둔다.

time T를 정해두고 T스텝까지만 진행하고 중단하는 방법이 있고,

임시 저장공간의 크기를 정해두고 저장공간이 꽉 차면 중단하는 방법이 있다.



![image-20210217114407211](images/image-20210217114407211.png)

![image-20210217114747987](images/image-20210217114747987.png)

그런데 단순히 log확률 값이 가능 큰 y를 출력하면 길이가 짧은 문장들이 나올 확률이 높기때문에 문장의 길이로 나누어주는 normalize를 한다.

![image-20210217114923581](images/image-20210217114923581.png)

### 3.BLEU score

output의 정확도를 평가하는 방법이다.

단순히 time step별로 단어를 맞췄는지만 평가하게 되면 단어가 한칸씩 밀리거나 한 단어만 빼먹은 경우라도 정확도가 0%가 될수있다.

![image-20210217115255248](images/image-20210217115255248.png)

정밀도는 (맞춘 단어의 수) / (예측한 문장의 길이)

재현율은 (맞춘 단어의 수) / (reference 문장의 길이)

F-measure 는 정밀도와 재현율의 조화평균이다.

그런데 이 방법은 단어의 순서와 상관이 없다.

![image-20210217115629249](images/image-20210217115629249.png)



![image-20210217120037896](images/image-20210217120037896.png)

순서를 반영하지 못하는 방법을 개선한 것이 BLEU score이다

N-gram 단위로 존재하는지를 측정한다. (N = 1,2,3,4)

![image-20210217120615216](images/image-20210217120615216.png)

## 참고용

- [Sequence to sequence learning with neural networks, ICML’14](https://arxiv.org/abs/1409.3215)
- [Effective Approaches to Attention-based Neural Machine Translation, EMNLP 2015](https://arxiv.org/abs/1508.04025)
- [CS224n(2019)_Lecture8_NMT](https://web.stanford.edu/class/cs224n/slides/cs224n-2019-lecture08-nmt.pdf)

- [Deep learning.ai-BeamSearch](https://www.youtube.com/watch?v=RLWuzLLSIgw&feature=youtu.be)
- [Deep learning.ai-RefiningBeamSearch](https://www.youtube.com/watch?v=gb__z7LlN_4&feature=youtu.be)
- [OpenNMT-beam search](https://opennmt.net/OpenNMT/translation/beam_search/)

## 궁금한 점

