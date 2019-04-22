---
layout: post
title: "PAC Learning"
subtitle: "PAC Learning"
categories: data
tags: ml
comments: true
---

## PAC (Probably Approximately Correct) Learning
머신러닝 모델을 생각했을 때, 어떠한 condition에서 성공적인 learning 이 나올까? 또한, 어떠한 condition에서 learning algorithm이 잘 작동할까?
이러한 이슈를 수학적으로 분석하는 framework들 중 하나인 PAC learning을 오늘 설명해보자 한다.
PAC learning이란 '높은 확률로 (Probably)' 주어진 모델이 '작은 error를 가진다 (Approximatly Correct)'와 같은 식의 분석을 한다. 

PAC learning을 설명하기 앞서 먼저 사용되는 notation들을 정의해보자
- X
- c
- C
- T
- S
- H

Notation을 정리하였으니 이제 PAC bound를 정의하기 위해 사용되는 4가지 요소를 알아보고자 한다.
- $$m$$: training data의 샘플 수 
- $$\varepsilon$$: misclassification error rate
	- train error 와 true(test) error의 gap이라고도 불린다.  $$error_{true}(h) \leq error_{train}(h) + \varepsilon$$
- $$|H|$$: hypothesis space의 complexity
- $$$(1-\delta)$: confidence of the relation. 알고리즘이 $\varepsilon$$과 $$\delta$$를 사용하여 'probably correct'이기 위한 least 값

이러한 4가지 요소를 사용하여 PAC bound는 다음과 같이 정의가 된다.
$$Pr[error_{true}(h) \leq error_{train}(h) + \varepsilon] \leq ||H||\exp(-2m\varepsilon^2) $$


