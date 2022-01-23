

# Anomaly Detection

- 오류를 탐지하기 위한 알고리즘이 아니라, 전체 데이터 중 매우 작은 비율을 갖는 한쪽 데이터인 'skewed class'를 검출하는 알고리즘이다. 

1. #### 지도 학습 (Supervised Learning)

   지도 학습은 주어진 Training Dataset에 정상 샘플과 비정상 샘플 의 data와 label이 모두 존재하는 학습 방법이다. 비정상 샘플을 다양하 게 보유하거나 패턴이 크게 다른 물체를 분류하는 경우에는 분류가 쉽지 만 정상 샘플보다 비정상 샘플의 발생 빈도가 적은 Class Imbalance 문제를 겪게 되어 학습이 제대로 이루어지지 않을 수 있다.

2. #### 준지도 학습 (Semi-supervised Learning)

   Class-Imbalance가 매우 큰 경우 정상 샘플만 이용해서 모델을 학 습하기도 하는데, 이를 준지도 학습이라고 한다. 이 방법론은 label이 표 시된 데이터와 표시되지 않은 데이터를 모두 훈련에 사용하는 것이다. 대표적인 연구로 딥러닝을 기반으로 One-Class Classification 방법론 을 사용하는 Deep SVDD[2]이 있다. 정상 샘플만 있어도 학습이 가능 하다는 장점이 있지만 지도학습 방법론에 비해 상대적으로 판정의 정확 도가 떨어진다는 단점이 있다

3. #### 비지도 학습 (Unsupervised Learning)

   위의 학습 방법들은 수많은 샘플 중 어떤 것이 정상 샘플인지 알기 위해서 반드시 정상 샘플에 대한 label을 얻는 과정이 필요하다. 이러한 점 때문에 대부분의 데이터가 정상 샘플이라는 가정을 하여 label 취득 없이 학습을 시키는 비지도 학습 기반 이상치 탐지 방법론을 고려할 수 있다. 비지도 학습 기반 이상치 탐지를 위해 대표적으로 오토인코더 (Autoencoder)를 이용하여 결함(비정상)을 찾아내는 연구가 대표적으로 이루어지고 있다.

## U-Net 네트워크를 통한 이상치 탐지 

오토인코더는 입력을 압축하는 Encoding과, 이를 다시 원본과 가 깝게 복원해내는 Decoding 과정으로 진행이 되며 이를 통해 데이터의 중요한 정보들만 압축적으로 학습할 수 있는 네트워크이다. 학습된 모델 에 비정상 이미지가 들어왔을 때 출력 값과 입력 값의 차이가 클 것이라 는 것을 가정하였고 입력 값 대비 출력 값이 다른 정도에 따라 비정상으 로 판단할 수 있다. 하지만 오토인코더를 기반으로 한 네트워크는 Encoding과 Decoding 과정에서 차원 축소로 인한 정보의 손실을 가져 와 정확도가 높지 않고, 하이퍼파라미터 값에 민감하다는 단점을 지닌 다. 그런 이유로 본 논문에서는 공간 정보 손실을 방지할 수 있도록 개선 된 네트워크인 U-Net을 활용하기로 하였다. Decoding 영역에서의 Pooling Layer를 Up-sampling 영역으로 대체하고 Encoding 영역에 서 출력된 결과물을 Decoding 영역과 Concat함으로써 이미지 크기에 관계없이 적용 가능하며 Localization과 Context 인식에 모두 좋은 성능을 보여주어 본 실험에서의 인쇄물 패턴 검출에 적합하다고 판단하였 다. 

## U-net

Encoder ━ Decoder 형태를 가진 모델 중 하나이면서, 바이오메디컬 이미지 Segmentation에 있어 상당한 성능을 보이는 모델이다. U-Net을 설명하는 논문에서는 Encoder 과정을 Contracting Path, Decoder 과정을 Expanding Path라고 부른다. 

<img src="https://mblogthumb-phinf.pstatic.net/MjAyMDA2MDhfMjk2/MDAxNTkxNTk5NDM1OTE2.EIVQDNmNatqHtY9Esfhgdlc992-bNX5KrKaE1msGGAMg.UUW1ZbibI_9hA5vxnPqjGvEIj_6Dp_CtMuyUNBwI3UUg.PNG.9709193/unet.png?type=w800">













참고문헌 : Anomaly Detection in printed patters using U-Net(Hong, Soon-Hyun　　Nam, Hyeon-Gil 　　Park, Jong-Il Hanyang University)
