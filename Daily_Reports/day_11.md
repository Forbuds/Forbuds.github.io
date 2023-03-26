
---
title: "Day 011"
date: 2023-03-21

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크럼
노션에 기록
- [ ]  transformer 용어 정리  
- [ ]  transformer 논문읽기  
- [x]  백준  
- [x]  [딥러닝 기본] 강의 듣기  
- [x]  [딥러닝 기본] 실습  
- [x]  [딥러닝 기본] 과제  
- [x]  캠퍼 주간 피드백  
- [ ]  [LSTM] 강의 듣기  
- [ ]  [LSTM] 실습  
- [ ]  [Transformer] 강의 듣기  
- [ ]  [Transformer] 실습   

## 01. Course

✅ 딥러닝이란?  
- Data, model, loss function, algorithm    
-  인공지능 : 사람의 지능을 모방한다  
-  머신러닝: 학습은 데이터를 가지고  
-  딥러닝 ; 뉴럴 네트워크로 어떻게 해 보자  
행렬은 두 개의 vector space 사이의 변환으로 이해하자  

✅ 뉴럴 네트워크 / MLP  
딥러닝의 목적은 loss를 무조건적으로 줄이는 것이 아니라 처음 보는 데이터에서도 잘 동작하도록 하는 것  
-   **그래서 사용할 전략은 백프로파게이션 : loss 함수를 줄이는 것이 목표**  
-   **나의 파라미터가 어느 방향으로 움직였을 때 loss fuction이 줄어드는지? 알고 그 뱡향으로 파라미터를 바꾸는 것이 목표이다.**  
-   **그래서 loss function이 줄어드는게 목적이니까 각각의 파라미터로 미분해서 음수 방향으로 밀어가면서 업데이트**    
-   **이렇게 하면 loss가 최소화되는 어떤 지점까지 도달하게 된다.**  
-   **이렇게 w와 b를 계속 업데이트해 나가는 것을 gradient decent라고 한다.**  

✅ MLP     
입력 → 리니어 변환 or affine transform → 히든 벡터 → 변환 → output  
한 단 짜리 히든 레이어  

## 02. 피어 세션
**❓ detach()**  

**❓ 가중치 초기화(Weight Initialization) 설명**  
<[https://huangdi.tistory.com/8](https://huangdi.tistory.com/8)>  
<[https://hanlyang-0508.tistory.com/32](https://hanlyang-0508.tistory.com/32)>  


[**파이토치 전체 과정 리뷰 함께 하기**](https://github.com/victoresque/pytorch-template)  

## 05. 학습 회고
간단한 딥러닝 모델 빌드 예제가 과제로 주어졌는데, 서로 질문하는 시간을 가졌다. 이 부분에서 내가 스쳐지나갔던 부분을 팀원들이 피어 세션에서 질문해 나도 공부할 수 있었다.
