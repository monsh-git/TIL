---
layout: post
title:  "ARIMA Model - 1"
date:   2020-09-17 23:30:00 +0900
categories: TIL
---
ARIMA 모델은 데이터 특성을 탐  
그래서, Stationary 데이터에 적용을 함  

# Stationary 데이터  
연속 되는 숫자들의 평균, 분산, 공분산이 시간에 따라서 변하지 않아야 함  
쉽게 말해 트렌드가 있다는 것임  

# Dickey-Fuller Test  
데이터가 stationary한지 테스트 가능  

**Non-stationary 데이터도 differencing을 통해서 stationary하게 만들 수 있다.**  
**(ARIMA 모델 사용 가능하게 만들 수 있다)**

# Differencing은 3차 이상 하지 않는다  
트렌드와 seasonality를 제거하는 과정이기 때문  
트렌드나 seasonality가 있는 데이터를 그 이전 랙과의 차를 구했는데 트렌드나 seasonality가 없어지지 않는다?  
그것은 트렌드나 seasonality가 있는 게 아니기 때문...  
그런 데이터를 3차 이상 해 봐야 그것은 잘못된 경우다.  
보통 1~2차에서 끝나고, Seasonal Differencing을 따로 반복해서 조합함  

# Seasonal vs Non-seasonal  

# Using in Python  
forecast는 파라미터로 예측할 데이터의 개수를 받음  
  
ARIMA의 predict는 파라미터로 예측할 데이터의 인덱스를 받고,  
마지막으로 여러 개의 데이터를 예측하기 위해  
dynamic이라는 파라미터를 받음 (ARIMA 모델은 기본적으로 한 스텝만 예측할 수 있음)  
