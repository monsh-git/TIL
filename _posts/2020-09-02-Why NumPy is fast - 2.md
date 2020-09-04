---
layout: post
title:  "Why NumPy is fast - 2"
date:   2020-09-02 19:59:00 +0900
categories: TIL
---
![Diffence between ndarray and Python's list](https://image.slidesharecdn.com/numpy20160519-160516164831/95/numpy-8-638.jpg)  

# 파이썬 list가 느린 이유
- 파이썬 리스트는 결국 포인터의 배열  
- 경우에 따라서 각각 객체가 메모리 여기저기 흩어져 있음  
- 그러므로 캐시 활용이 어려움  

# NumPy ndarray가 빠른 이유
- ndarray는 타입을 명시하여 원소의 배열로 데이터를 유지  
- 다차원 데이터도 연속된 메모리 공간이 할당됨  
- 많은 연산이 dimensions과 strides를 잘 활용하면 효율적으로 가능  
    - 가령 transpose는 strides를 바꾸는 것으로 거의 공짜
- ndarray 구현 방식을 떠올리면 어떻게 성능을 낼 수 있는지 상상 가능  