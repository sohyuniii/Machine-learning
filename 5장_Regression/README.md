# Chapter5. Regression
- 주어진 피처와 결정 값 데이터 기반에서 학습을 통해 최적의 회귀계수 찾기!
- 종류로는 ***일반선형회귀, Ridge, Lasso, ElasticNet, Logistic Retression***

## [5.1 Gradient Descent](https://github.com/sohyuniii/Machine-learning/blob/master/5%EC%9E%A5_Regression/5.1%20Gradient%20Descent.ipynb)
- RSS를 최소로하는 회귀 계수를 찾고, 회귀에서 RSS를 **비용함수, 손실함수(loss ftn)** 라고 한다.
- 함수의 기울기를 구하여 기울기가 낮은 쪽으로 계속 이동시켜서 극값에 이를 때까지 반복시켜 RSS를 최소화시키는 값을 찾는 방법
- ***확률적 경사 하강법(stochastic gradient descent)***
  - 일반적으로 경사 하강법은 모든 학습 데이터에 대해 반복적으로 비용함수를 최소화 -> 수행시간 길다
  - 확률적 경사 하강법은 일부 데이터만 이용해 계산

## [5.2 Linear Model](https://github.com/sohyuniii/Machine-learning/blob/master/5%EC%9E%A5_Regression/5.2%20Linear%20Model.ipynb)
- LinearRegression()을 이용해 성형 회귀 모델 fitting
- 예측값과 실제 값의 RSS를 최소화해 OLS 추정 방식으로 회귀계수 
- Boston data를 이용하여 보스턴의 주택 가격 에측 : shape (506,14)

## [5.3 Over&Underfitting](https://github.com/sohyuniii/Machine-learning/blob/master/5%EC%9E%A5_Regression/5.3%20Over%26Underfitting.ipynb)
- ***Bias-Variance Trade off***
  - bias는 잘못된 가정을 했을 때 발생하는 오차, 높은 편향값은 underfitting 문제를 발생 
  - variance는 트레이닝 셋에 내재된 작은 변동 때문에 발생하는 오차, 높은 분산값은 큰 노이즈까지 모델링에 포함시키는 overfitting 문제를 발생 
