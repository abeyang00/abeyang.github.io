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

PAC bound를 정의하려면 PAC learning에 사용되는 4가지 요소를 알아야한다.
- $m$: training data의 샘플 수 
- $\varepsilon: misclassification error rate$
	- train error 와 true(test) error의 gap이라고도 불린다.  $\mbox{error}_{true}(h) \leq \mbox{error}_{train}(h) + \varepsilon$
- $|H|$ hypothesis space

