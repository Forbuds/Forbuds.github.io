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
- [x]  BFS 2문제
- [x]  심화과제 2
- [x]  AIMath 9,10  (10 정리는 내일)
- [ ]  Python 강의

## 01. Course
**CNN 첫 걸음**  
앞서 배운 다층 신경망(MLP)는 각 뉴런들이 선형 모델과 활성 함수로 모두 연결된 구조였음 ( fully connected)  
🔥$$h_{i} = \sigma(\sum_{j=1}^{p}W_{ij}x_{j})$$  
🔥여기서 $\sigma$가 활성 함수, W가 가중치 행렬 
    🔥가중치 행렬의 사이즈가 커지게 된다.  
    
🔥<span style="background-color:#ffdce0">Convolution</span>  연산은 이와 달리 <span style="background-color:#ffdce0">커널(Kernel)을 입력벡터 상에서 움직여</span>  가면서 <span style="background-color:#f7ddbe">선형모델과 함성함수가 적용</span> 되는 구조입니다.  
🔥$$h_{i} = \sigma(\sum_{j=1}^{k}V_{j}x_{i+j-1})$$  
🔥활성화 함수를 제외한 convolutinon 연산도 선형변환에 속한다.  
🔥<span style="background-color:#ffdce0">차이점 : i에 따라서 가중치 행렬이 바뀌는게 아니라 적용된 커널을 움직여 가면서 적용</span>  
파라미터 개수 줄인다!  
    🔥커널은 정의역 내에서 움직여도 변하지 않고 (translation invariant) 주어진 신호에 국소적(local)으로 적용합니다.  
    🔥 커널이 위치에 따라서 바뀌지 않는다!  
커널과 입력은, 행렬연상이 아니라 elementation 하게 곱셈을 하고 덧셈을 한다.  (모양은 행렬이지만)  

**RNN 첫 걸음**  
강의만 듣고 정리는 하지 않음

## 02. 피어 세션
심화과제 2에 대한 리뷰
표본분산을 구할 때 n이 아닌 n-1로 나눠주는 이유에 대한 토론 (아래 블로그를 팀원이 찾았는데, 굉장히 설명이 잘 되어 있다!)  
내가 찾은 블로그 : [자유도Degree-of-Freedom에서-자유로워-지기](https://diseny.tistory.com/entry/%EC%9E%90%EC%9C%A0%EB%8F%84Degree-of-Freedom%EC%97%90%EC%84%9C-%EC%9E%90%EC%9C%A0%EB%A1%9C%EC%9B%8C-%EC%A7%80%EA%B8%B0)  

먼저, 보통의 표본분산에 대한 설명은 
$$s^2 = \frac{\sum (y_{i}-\bar{y})^2}{n-1}$$  
$$\sigma ^{2} = \frac{\sum (Y_{i}-\bar{\mu })^2}{N}$$ 이건 모분산  
모집단에서 임의적으로 추출된 표본은 모집단보단 좁은 영역으로 뽑힐 수 밖에 없기 때문에 데이터간의 편차 (bias)가 적다. 
따라서 모분산을 추정하기 위해선 최대한 가깝게 추정해야 하니까 n보다 작은 값으로 나눠져 편차를 키워 보정이 들어가야 한다.  **불편추정값**
그렇게 해서 $$E(s^2) = E(\frac{\sum (y_{i}-\bar{y})^2}{n-1})= \sigma ^2$$ 이 수식이 나오고,  
"표본분산의 기대값은 모분산 $$\sigma ^2$$ 과 동일"


[왜 표본분산은 n-1로 나누죠 자유도 불편추정량에 대한 고백](https://recipesds.tistory.com/entry/%EC%99%9C-%ED%91%9C%EB%B3%B8%EB%B6%84%EC%82%B0%EC%9D%80-n-1%EB%A1%9C-%EB%82%98%EB%88%84%EC%A3%A0-%EC%9E%90%EC%9C%A0%EB%8F%84-%EB%B6%88%ED%8E%B8%EC%B6%94%EC%A0%95%EB%9F%89%EC%97%90-%EB%8C%80%ED%95%9C-%EA%B3%A0%EB%B0%B1)  
[n-1은 왜 자유도라고 불리는가요 자유도의 정체와 직관적인 이해](https://recipesds.tistory.com/entry/n-1%EC%9D%80-%EC%99%9C-%EC%9E%90%EC%9C%A0%EB%8F%84%EB%9D%BC%EA%B3%A0-%EB%B6%88%EB%A6%AC%EB%8A%94%EA%B0%80%EC%9A%94-%EC%9E%90%EC%9C%A0%EB%8F%84%EC%9D%98-%EC%A0%95%EC%B2%B4%EC%99%80-%EC%A7%81%EA%B4%80%EC%A0%81%EC%9D%B8-%EC%9D%B4%ED%95%B4)  
자유도에 대한 이해 : n개로 이루어진 표본의 표본평균을 이미 구했다면, 분산을 구하기 위해서는 n-1개까지만 구해도 나머지 1개의 표본 데이터를 추정할 수 있다. 그래서 자유도는 n이 아니라 n-1이 되는 것이다.  
그래서 이제 표본분산을 구해줄 때는 n이 아니라, n-1로 나눠준단다.  
-> 그런데 갑자기 드는 의문은, 그렇다면 모분산의 자유도는 왜 n일까? (해결 못함 ㅎㅎ)  

통계에 대한 블로그
- <https://recipesds.tistory.com/>
- <https://ko.khanacademy.org/math/statistics-probability/summarizing-quantitative-data/variance-standard-deviation-sample/a/population-and-sample-standard-deviation-review>

## 03. 마스터 클래스 - 임성빈 교수님

수학을 어떻게 하면 쉽게 이해할 수 있을까   
    →수학은 이해보단 익숙해지는 학문인 것 같다. (폰 노이만)  
    →많이 보는 것보다 많이 사용해 보는 게 좋다.  (예제를 사용해서 공부해야 한다.)  
모델들의 수학적 원리를 모두 알아야 하느냐?  
   →적어도 원리를 이해하는데 필요한 기초는 갖춰야 한다  
어느 분야가 기초일까?  
   →대학교 2-3학년 : 선형 대수, 확률론, 통계학  
   →알고리즘 최적화 기초  
기초 내용만 공부하기보단 머신러닝에서 어떻게 활용되는지 검색해봅시다  
    →분류 문제에서 왜 ce를 손실함수로 사용되는가?  
    →경사 하강법을 쓰는 것보다 anj  
ML 엔지니어는 수학을 어느 정도 알아야  할까요?  
    →필요한 걸 공부해서 빠르게 따라잡을 수 있을 만큼  
    →문제를 해결하고자 하는 단초 /문제를 바랍보는 프레임워크를  
엔지니어는 어떤 사람일까?  
    →남들 코드 : 서비스를 만드는 사람  
    →내가 다루는 문제를 내 방법론들을 조합할 수 있는 사람  
문제 정의와 brainstorm : 이 step에서 수학적인 기초가 많이 필요하다.  
**알고리즘 최적화**  -> 엔지니어로써 중요한 과목이다  
논문은 같이 읽어야 서로 구멍을 메꿔줄 수 있다. 혼자보다는 여럿이서 같이 읽는 그룹 스터디  
    →혹은 논문 같이 읽는 유튭도 있다. (*주의)  
논문 읽기 순서?   
   →인용이 가장 많이 되는 논문부터 시작해서 차츰 추가해 나가는 것이 좋을 것 같다.  
어떤 데이터 (사이언스는 엔지니어 일도 할 수 있어야 한다.)  
**논문 구현 (코드로) 한꺼번에 코드와 논문을 구현해 보는게 굉장히 중요하다.**  

## 04. 학습 회고
PS를 생각보다 다시 까먹어서 정리해가면서 기본 문제도 푸는 형식으로 해 나가야 겠다는 생각이 들었다.
그리고 BFS, DFS를 다시금 매주 풀어가야 겠다고 생각이 들었다.

