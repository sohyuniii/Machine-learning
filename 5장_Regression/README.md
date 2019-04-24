# Chapter5. Regression
- 주어진 피처와 결정 값 데이터 기반에서 학습을 통해 최적의 회귀계수 찾기!
- 종류로는 ***일반선형회귀, Ridge, Lasso, ElasticNet, Logistic Retression***

## [5.1 Gradient Descent](https://github.com/sohyuniii/Machine-learning/blob/master/5%EC%9E%A5_Regression/5.1%20Gradient%20Descent.ipynb)
- RSS를 최소로하는 회귀 계수를 찾고, 회귀에서 RSS를 **비용함수, 손실함수(loss ftn)** 라고 한다.
- 함수의 기울기를 구하여 기울기가 낮은 쪽으로 계속 이동시켜서 극값에 이를 때까지 반복시켜 RSS를 최소화시키는 값을 찾는 방법
- ***확률적 경사 하강법(stochastic gradient descent)***
  - 일반적으로 경사 하강법은 모든 학습 데이터에 대해 반복적으로 비용함수를 최소화 -> 수행시간 길다
  - 확률적 경사 하강법은 일부 데이터만 이용해 계산
