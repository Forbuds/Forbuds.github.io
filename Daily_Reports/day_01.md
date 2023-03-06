---
title: "Day 001"
date: 2023-03-06

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---
[![Peer session bedge](https://img.shields.io/badge/peer%20session-B1FD8F?style=flat)](https://forbuds.github.io/peer_session/D_001.html)
## 00. 타운 홀 미팅
- 기록과 자기만의 이야기를 만들어 갔으면 좋겠다.
- 주의사항
    - 지식은 공유 가능, 그렇지만 과제를 전부 보여 주지는 x 
    - 오픈소스는 출처 명시
    - 실수로 학습 시작 & 학습 종료하지 않게 노력하기
    - 블로그 회고 가능, 콘텐츠는 업로드 불가 (코드 그대로, pdf그대로 안됨)
- 외출 기록 방법은 학습 종료 누르고 볼일 보고 학습 시작
-  스페셜 피어 세션 매 주 다른 분들과 함께 진행된다.
-  강의 질문 게시판 Q&A 상시 업로드 가능, 공지 참고해서 작성
-  slack 질의 응담 : #03 운영 질의 응답
-  zoom : 베이스 캠프 세팅, 정해진 시간 외에 배정된 팀 채널로 가능 (#04랜덤 채널에서 예약 가능)
-  점심은 따로 외출 처리 안해도 됨
-  공결은 최소 3일 전에 / 갑자기 일이 생기면 당일에라도, 증빙문서는 당일 혹은 다음날까지 가능

## 01. Course
코사인 법칙이 갑자기 생각이 안났다  
$$cos(\theta)=\frac{\left\| x\right\|_{2}^{2}+\left\| y\right\|_{2}^{2}-\left\| x-y\right\|_{2}^{2}}{2\left\| x\right\|_{2}^{2}\left\| y\right\|_{2}^{2}}$$   
$$cos(\theta)=\frac{2<x,y>}{2\left\| x\right\|_{2}\left\| y\right\|_{2}}$$  , 이때 $$<x,y>$$ 는 $$\sum_{i=1}^{d}x_{i}y_{i}$$  

분류 문제를 풀려면 softmax함수를 풀어야 한다. (모델의 출력을 확률로 해석할 수 있게 변환해 주는 연산!)  
But, 학습은 Softmax, 추론은 one hot  

딥러닝, 신경망 <span style="background-color:#ffdce0">"선형 모델의 출력물 + 활성화 함수"</span>*(딥딥)  

활성 함수 (Activation function)  
- 비선형 함수
    - 시그모이드 : $$\sigma (x) = \frac{1}{1+e^{-x}}$$
    - tanh : $$tanh(x)=\frac{e^{x}-e^{-x}}{e^{x}+e^{-x}}$$
    - ReLU : $$ReLU(x)=max\left\{0,x \right\}$$

딥러닝 과정 : 순전파 + 역전파
- 순전파
    - 신경망 계산 (입력 -> 선형 모델 -> 활성화함수 -> 출력)
- 역전파
    - <span style="background-color:#ffdce0">체인 룰!</span>
    - 가중치 행렬에 대한 gradient벡터 계산해서 경사하강법  

## 02. 피어 세션
모더레이터 선정 : 사다리 타기  
피어 세선 그라운드 룰 정하기  
- 우리 팀원을  소개합니다.  
    - 각자의 이름, MBTI, 취미, 나이, 부캠에서 얻어가고 싶은 점 작성
- 아침 모닝콜 : 10:00
    - 1000원
    - 전날에 말하면 오케이 
- 줌공 시간 정하기 : 10:00~12:00 , 2:00~5:00
- PS 같이 하기 
    - 일주일에 다섯 문제 
    - https://www.acmicpc.net/workbook/by/BaaaaaaaaaaarkingDog
    - 1. BFS 2.재귀 3. 백트래킹 4. 그리디 5. DP

## 03. 과제 수행 과정/과제 결과물에 대한 정리
이미지 데이터를 나타내는 형렬을 이동시키기 위해서는 <span style="background-color:#ffdce0">행렬의 곱셈</span>이 사용된다!  
이미지를 <span style="background-color:#ffdce0">평행이동 시키는 연산자로서</span>의 행렬을 완성하는 과제  $$e@f$$  
$$f = \begin{bmatrix}
 0& 1 & 0 \\
 0& 0 &  1\\
 1& 0 & 0 \\
\end{bmatrix}$$  
이미지를 <span style="background-color:#ffdce0">좌우로 대칭이동 시키는 연산자</span>로서의 행렬을 완성하는 과제 $$e@f$$  
$$f = \begin{bmatrix}
 0& 0 & 1 \\
 0& 1 &  0\\
 1& 0 & 0 \\
\end{bmatrix}$$

## 04. 학습 회고
첫 날이라 강의는 많이 듣지 못했고, 적응하는 시간이었던 것 같다. 강의에서 나온 코드들을 다 구현해 보고 싶은데 시간이 허락해 줄 지 모르겠다.
