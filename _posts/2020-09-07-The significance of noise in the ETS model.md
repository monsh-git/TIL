---
layout: post
title:  "The significance of Noise in the ETS model"
date:   2020-09-07 22:19:00 +0900
categories: TIL
---
Seasonal decompose를 해서, error(noise)를 추출할 수 있는데,  
이 때, 이 **noise(error)에서도 패턴을 발견**할 수 있다.  
이후, **모델링된 noise에 seasonality와 trend를 더하는 과정을 통해서**  
prediction을 하게 된다.