---
title: "Day 004"
date: 2023-03-09

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크림
노션에 기록
- [x]  BFS 1문제
- [x]  심화과제 2
- [x]  AIMath 9,10  (10 정리는 내일)
- [ ]  Python 강의

## 01. Course


## 02. 피어 세션
심화과제 2에 대한 리뷰
표본분산을 구할 때 n이 아닌 n-1로 나눠주는 이유에 대한 토론 (아래 블로그를 팀원이 찾았는데, 굉장히 설명이 잘 되어 있다!)  
내가 찾은 블로그 : <https://diseny.tistory.com/entry/%EC%9E%90%EC%9C%A0%EB%8F%84Degree-of-Freedom%EC%97%90%EC%84%9C-%EC%9E%90%EC%9C%A0%EB%A1%9C%EC%9B%8C-%EC%A7%80%EA%B8%B0>  

먼저, 보통의 표본분산에 대한 설명은 
$$s^2 = \frac{\sum (y_{i}-\bar{y})^2}{n-1}$$  
$$\sigma ^{2} = \frac{\sum (Y_{i}-\bar{\mu })^2}{N}$$ 이건 모분산  
모집단에서 임의적으로 추출된 표본은 모집단보단 좁은 영역으로 뽑힐 수 밖에 없기 때문에 데이터간의 편차 (bias)가 적다. 
따라서 모분산을 추정하기 위해선 최대한 가깝게 추정해야 하니까 n보다 작은 값으로 나눠져 편차를 키워 보정이 들어가야 한다.  **불편추정값**
그렇게 해서 $$E(s^2) = E(\frac{\sum (y_{i}-\bar{y})^2}{n-1})= \sigma ^2$$ 이 수식이 나오고,  
"표본분산의 기대값은 모분산 $$\sigma ^2$$ 과 동일"


<https://recipesds.tistory.com/entry/%EC%99%9C-%ED%91%9C%EB%B3%B8%EB%B6%84%EC%82%B0%EC%9D%80-n-1%EB%A1%9C-%EB%82%98%EB%88%84%EC%A3%A0-%EC%9E%90%EC%9C%A0%EB%8F%84-%EB%B6%88%ED%8E%B8%EC%B6%94%EC%A0%95%EB%9F%89%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B3%A0%EB%B0%B1>  
<https://recipesds.tistory.com/entry/n-1%EC%9D%80-%EC%99%9C-%EC%9E%90%EC%9C%A0%EB%8F%84%EB%9D%BC%EA%B3%A0-%EB%B6%88%EB%A6%AC%EB%8A%94%EA%B0%80%EC%9A%94-%EC%9E%90%EC%9C%A0%EB%8F%84%EC%9D%98-%EC%A0%95%EC%B2%B4%EC%99%80-%EC%A7%81%EA%B4%80%EC%A0%81%EC%9D%B8-%EC%9D%B4%ED%95%B4>  
자유도에 대한 이해 : n개로 이루어진 표본의 표본평균을 이미 구했다면, 분산을 구하기 위해서는 n-1개까지만 구해도 나머지 1개의 표본 데이터를 추정할 수 있다. 그래서 자유도는 n이 아니라 n-1이 되는 것이다.  
그래서 이제 표본분산을 구해줄 때는 n이 아니라, n-1로 나눠준단다.  
-> 그런데 갑자기 드는 의문은, 그렇다면 모분산의 자유도는 왜 n일까? (해결 못함 ㅎㅎ)  

통계에 대한 블로그
- <https://recipesds.tistory.com/>
- <https://ko.khanacademy.org/math/statistics-probability/summarizing-quantitative-data/variance-standard-deviation-sample/a/population-and-sample-standard-deviation-review>

## 03. 과제 수행 과정/과제 결과물에 대한 정리

- <span style="background-color:#ffdce0">$$x_{t+1} \leftarrow x_{t+1}-lr*{f}^{'}(x_{t})$$</span>  
## 04. 학습 회고

