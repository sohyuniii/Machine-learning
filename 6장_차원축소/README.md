# Chpater6. 차원 축소  
- 차원축소란? 많은 피처로 구성된 다차원 데이터의 차원을 축소해 새로운 차원의 데이터셋을 생성하는 것
- 차원이 증가할수록 데이터 간의 거리가 기하급수적으로 멀어지고, sparse한 구조를 갖게 된다.
- ***피처 선택 (feature selection)***
  - 특정 피처에 종속성이 강한 불필요한 피처는 아예 제거하고, 데이터의 특징을 잘 나타내는 주요 피처만 선택
- ***피처 추출 (feature extraction)***
  - 기존 피처를 저차원의 중요 피처로 압축해서 추출하는 것
  - 단순압축이 아닌, 피처를 함축적으로 더 잘 설명할 수 있는 또다른 공간으로 매핑하여 추출 -> 잠재적인 요소 추출 
  
## [6.1 PCA(Principal Component Analysis)]()
- 여러 변수 간에 존재하는 상관관계를 이용해 이를 대표하는 주성분을 출해 차원을 축소
- 가장 높은 분산을 가지는 데이터의 축을 찾아 이 축으로 차원을 축소

## [6.2 LDA(Linear Discriminant Analysis)](https://github.com/sohyuniii/Machine-learning/blob/master/6%EC%9E%A5_%EC%B0%A8%EC%9B%90%EC%B6%95%EC%86%8C/6.2%20LDA(Linear%20Discriminant%20Analysis).ipynb)
- 클래스 간 분산과 클래스 내부 분산의 비율을 최대화하는 방식으로 차원을 축소
- 클래스 간분산은 MAX, 클래스 내부의 분산은 MIN

## [6.3 SVD & NMF]()
- ***SVD(Singular Value Decomposition)***
  - PCA의 경우 정방행렬만을 고유벡터로 분해할 수 있지만, SVD는 아니여도 가능
- ***NMF(Non-Negative Matrix Factorization)***
  - 낮은 랭크를 통한 행렬 근사 방식의 변형
  - 원본 행렬 내의 모든 원소 값이 모두 양수일 때 사용

## Default of credit card clients [Data](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)
