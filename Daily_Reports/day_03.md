---
title: "Day 003"
date: 2023-03-08

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크림
노션에 기록
- [ ]  AI Math : 8강-9강
- [ ]  심화문제 1 (3-1,4)
- [ ]  심화 문제 3
- [ ]  BFS 개념 되짚기
- [ ]  데일리 레포트 정리
- [ ]  과제 업로드

## 01. Course


## 02. 피어 세션



## 02. 과제 수행 과정/과제 결과물에 대한 정리

**Gradient Descent**  
- <span style="background-color:#ffdce0">$$x_{t+1} \leftarrow x_{t+1}-lr*{f}^{'}(x_{t})$$</span>  그래디언트 업데이트 식이다.
- 경사하강법의 핵심 구간. x에 해당하는 부분 업데이트
-<span style="background-color:#ffdce0"> **"경사"로 하강법 (-)**</span> 라고 생각하면서 개념이해를 하자.
```python
train_x = (np.random.rand(1000) - 0.5) * 10
train_y = np.zeros_like(train_x)

idx = np.random.choice(1000, 10, replace=False) # 10개 랜덤으로 뽑는다
#    array([713, 514, 965, 111, 407, 284, 523, 807,  94, 248])

mini_x = train_x[idx]
mini_x   #data [list] 이런 식으로 넣어주게 되면
#    array([-0.23951029, -3.84651565,  0.64575139, -1.55756678, -3.49724245,
#        3.26336952,  2.08369702,  3.79882649, -0.11643808, -4.77585745])
```
이렇게 

## 03. 학습 회고


