# Chapter7. Clutering
## [7.1 K-means](https://github.com/sohyuniii/Machine-learning/blob/master/7%EC%9E%A5_Clustering/7.1%20K-Means.ipynb)
- 군집 중심점(***centroid***)라는 특정한 임의의 지점을 선택해 해당 중심에 가장 가까운 포인트들을 선택하는 군집화 기법
- 군집 중심점은 선택된 포인트의 평균 지점으로 이동하고, 이동된 중심점에서 다시 가까운 포인트를 선택하는 프로세스를 반복적으로 수행 
- 거리 기반 알고리즘으로 속성의 개수가 매우 많을 경우 정확도 떨어진다 -> PCA

## [7.2 Cluster evaluation](https://github.com/sohyuniii/Machine-learning/blob/master/7%EC%9E%A5_Clustering/7.2%20Cluster%20evaluation.ipynb)
- 대부분의 군집화 데이터는 비교할 만한 타깃 레이블이 없다 -> 실루엣 분석 이용
- **실루엣 분석 (silhouette analysis)**
  - 각 군집 간의 거리가 얼마나 효율적으로 분리돼 있는지를 나타낸다.
  - a(i)는 같은 군집 내에 있는 다른 데이터와의 거리 평균, b(i)는 가장 가까운 다른 군집과의 평균 거리
   <img src="https://user-images.githubusercontent.com/41772329/57983149-92972d00-7a89-11e9-933f-4b3f7e788d15.png" width="30%">
  
  - -1~1의 값을 가지며 1로 가까울 수록근처의 군집과 더 멀리 떨어져 있다는 것을 의미

## [7.3 Mean Shift](https://github.com/sohyuniii/Machine-learning/blob/master/7%EC%9E%A5_Clustering/7.3%20Mean%20Shift.ipynb)
- k-means와 비슷하게 중심을 군집의 중심으로 지속적으로 움직이면서 군집화 수행
- 특정 대역폭(***bandwidth***)을 가지고 중심을 데이터가 모여 있는 밀도가 가장 높은 곳으로 이동
- bandwidth 값을 작게 할수록 군집 개수가 많아진다.
- 장점 : 모델을 가정하지 않으므로 좀 더 유연, 이상치의 영향력 크지 X, 군집 개수 정할 필요 X
- 단점 : 알고리즘의 수행 시간이 오래걸린다, bandwidth의 크기에 따른 군집화 영향도가 크다.
- 컴퓨터 비전 영역, 이미지나 영상 데이터에서 개체를 구분하거나 움직임을 추적하는 데 뛰어나다.
