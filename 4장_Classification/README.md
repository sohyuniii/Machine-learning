# Chapter4. 분류
## [4.1 Decision Tree](https://github.com/sohyuniii/Machine-learning/blob/master/4%EC%9E%A5_Classification/4.1%20Decision-Tree.ipynb)
- 데이터에 있는 규칙을 학습을 통해 자동으로 찾아낸 트리 기반의 분류 규칙을 만드는 것
- decision node는 규칙조건/ leaf node는 결정된 클래스 -> 트리가 깊어질수록 예측 성능이 저하될 가능성이 높다.
- 균일도 측정 방법 
  - entropy 지수 : 주어진 데이터 집합의 혼잡도로, 서로 다른 값이 섞여 있으면 엔트로피값이 높다.
  - 지니 계수 : 다양성이 낮을수록 균일도가 높다는 의미로, 1로 갈수록 균일도가 높다.
- **Parameter** (DecisionTreeClassifier 함수)
  - min_samples_split : 노드를 분할하기 위한 최소한의 샘플 데이터, 작게 설정할수록 과적합 (default 2)
  - min_samples_leaf : leaf가 되기 위한 최소한의 샘플 데이터 수
  - max_features : 고려할 최대 피처 갯수 (default None-모든피처사용)
  - max_depth : 트리의 최대 깊이, 깊어질수록 과적합(default None)
- **Data : [Human Activity Recognition](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones#)**
  - 30명에게 스마트폰 센서를 장착한 뒤 사람의 동작과 관련된 여러 가지 피처를 수집한 데이터
  - 사용자 행동인식 데이터에 대한 예측분류
