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
**Bayes' theorem**
🔥$$P(A|B)=\frac{P(A\cap B)}{P(B)}$$   
🔥$$P(A\cap B)=P(B)P(A|B)$$  
🔥베이즈 정리를 통해 새로운 데이터가 들어왔을 때 앞서 계산한 사후확률을 사전확률로 사용하여 갱신된 사후확률을계산 가능  
  
🔥실제로 설계를 false negative를 줄이는 방향으로 학습하긴 한다. (굉장히 민감하게 다룬다._)  

*공부할 때 블로그 보면서 참고할 것 (특히 그림)


## 02. 피어 세션
심화과제 1에 대한 질문 및 리뷰 
W,b의 업데이트에 관한 질문함
gradient 계산하는 과정 질문 -> X가 1c이 아닌, 2c로 이해해야 함.


## 03. 과제 수행 과정/과제 결과물에 대한 정리

**Gradient Descent**  
- <span style="background-color:#ffdce0">$$x_{t+1} \leftarrow x_{t+1}-lr*{f}^{'}(x_{t})$$</span>  그래디언트 업데이트 식이다.
- 경사하강법의 핵심 구간. x에 해당하는 부분 업데이트
- <span style="background-color:#ffdce0"> **"경사"로 하강법 (-)**</span> 라고 생각하면서 개념이해를 하자.
- 아래는 $${f}^{'}(x_{t})$$의 적용 방법이다.  

```python
#sym 사용
fun = sym.poly(x**2 + 2*x + 3)
diff = sym.diff(fun,x)
diff.subs(x, val)        # 이렇게 적용 하거나 

# 함수 사용              
result=(f(x+h)-f(x))/h  # h=1e-9
```
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

- 막간 꿀팁
  - ```python 
     train_x = np.array([1,2,3,4])
     w = 3.0
     b = 0.3
     print(train_x)
     print(train_x*w +b)

     # [1 2 3 4]
     # [ 3.3  6.3  9.3 12.3]   #브로드캐스팅
     ```


## 03. 학습 회고
경사 하강법을 실제 수식으로 (손으로) 풀이한 것을 한번 찾아봐야 겠다.
그런 후에 심화과제 3-1 다시 회고해 볼 것.
베이즈 정리 강의 재수강 할 것 (한번 훓긴 했지만 내용 하나하나 다시 정리해둘 것.)


