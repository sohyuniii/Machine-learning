# Chapter4. 분류
## [4.1 Decision Tree](https://github.com/sohyuniii/Machine-learning/blob/master/4%EC%9E%A5_Classification/4.1%20Decision-Tree.ipynb)
- 데이터에 있는 규칙을 학습을 통해 자동으로 찾아낸 트리 기반의 분류 규칙을 만드는 것
- decision node는 규칙조건/ leaf node는 결정된 클래스 -> 트리가 깊어질수록 예측 성능이 저하될 가능성이 높다.
- 균일도 측정 방법 
  - entropy 지수 : 주어진 데이터 집합의 혼잡도로, 서로 다른 값이 섞여 있으면 엔트로피값이 높다.
  - 지니 계수 : 다양성이 낮을수록 균일도가 높다는 의미로, 1로 갈수록 균일도가 높다.
- **Human Activity Recognition [Data](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#)**
  - 30명에게 스마트폰 센서를 장착한 뒤 사람의 동작과 관련된 여러 가지 피처를 수집한 데이터
  - 사용자 행동인식 데이터에 대한 예측분류

## 4.2 Ensemble
- 여러 개의 분류기(Classifier)를 생성하고 그 예측을 결합함으로써 보다 정확한 최종 예측을 도출하는 기법
- 앙상블 학습유형
  - [**Voting**](https://github.com/sohyuniii/Machine-learning/blob/master/4%EC%9E%A5_Classification/4.2.1%20Voting.ipynb) : 서로 다른 알고리즘을 가진 분류기를 결합
    - Hard Voting : 예측한 결과값들 중 다수의 분류기가 결정한 예측값을 최종 보팅 결과값으로 선정 
    - Soft Voting : 분류기들의 결정 확률을 모두 더하고 이를 평균해서 확률이 가장 높은 레이블 값을 최종 보팅 
  - **Bagging** : 각각의 분류기가 모두 같은 유형의 알고리즘 기반이지만, 데이터 샘플링을 서로 다르게 가져가면서 학습을 수행해 보팅을 수행하는 것 
    - [**Random Forest**]() : 기반 알고리즘은 decision tree, subset 데이터는 bootstrapping로 데이터 분리
  - **Boosting** : 여러 개의 분류기가 순차적으로 학습을 수행하되, 앞에서 학습한 분류기가 예측이 틀린 데이터에 대해서는 다음 분류기에게는 가중치를 부여하면서 학습과 예측을 진행 (ex : XGBoost, LightGBM)
