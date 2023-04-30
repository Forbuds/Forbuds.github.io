---
title: "Day 029"
date: 2023-04-13

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크럼  
노션에 기록

- [x]  BERT 논문 ( 오전 )  
- [x]  baseline 코드 분석  
- [x]  강의 들으면서 정리 (3강만)  

모각공 시간 다시 부할시켰다. 10시~12시, 2시~4시로 진행하였다.  

## 01. BERT 논문 요약
    
Notion에 정리  

## 02. 강의 정리    



신경망 분류 기법, N21 방법에 대한 강의를 수강하였다.  
흐름은 다음과 같다.
  1. 일단 N개의 class를 설계해야 한다.  
1. 신경망 디자인  
2. 입력을 문장 형태로  
3. 계산 (feed forward)  
4. Class별 Scoring  
   
❓ 그렇다면 어떻게 정답을 맞추는 방향으로 학습을 시킬 수 있을까?  
- Reference Representation  

  - 다음에 또 가려구요! [positive] : 이 positive라는 기호를 숫자 어떻게 표현할 것인가!  
  - label 데이터에는 일관성이 중요해서, one-hot 방법이 한계가 있지만 많이 사용한다.  
  
- Scoring Normalization  
  - 서로 다른 값들을 비교하기 위해서 같은 scale로 맞춰줘야 한다.  
  - 가장 많이 볼 수 있는게 <span style="background-color:#ffdce0">sofmax</span>  
    - 분모가 양수이면서 네 가지 클래스를 모두 합쳐주는 것  
    - 양수이면서 전체에 대한 비율  
    - <span style="background-color:#ffdce0">**-∞ ~ +∞ 로 나오는 값을 일종의 normalization하면서 0~1사이 값으로 바꿔 주는, 그것들의 합이 1.0을 넘지 않는 값들로 바꿔 주는 좋은 장치인 것이다.**</span>  
          
- Cost Function Design  
  - 예측값과 정답의 두 점수들 간의 차이를 어떻게 수치화 할 수 있을까?  
  - 관점에 따라 서로 다른 이름  
      - Error : 예측이 정답에 비해서 얼마나 오류가 있는지   
      - Cost : 기계가 내놓은 예측 값을 정답으로 바꾸기 위해서 얼마나 비용을 지불해야 하는지 (얼마만큼의 노력을 해야 하는지)  
      - Loss : 예측이 정답이랑 달라서 손실을 가지고 있다.  
      - Object : ML의 목적에 집중!  
  - 그런데 일단 조건 : **미분 가능**해야 한다.  
      - backpropagagte해서 파라미터를 업데이트해야한다.  
  - 분류 : cross entropy  
      - 예측을 하는 것도 확률 분포고, 정답도 확률 분포니까, 확률 분포간에 유사성을 비교하는 이미 잘 정리되어 있는 양방점수인 cross entropy를 쓰면 되겠구나  

- Parameter Update  

---

<span style="background-color:#ffdce0">**N21 : Encoder + fully connected layer**</span>  
- Topic classification, semantic textual similarity, ....  
1. Output이 숫자인 경우  
   - Regression  
   - Mean Squared Error   
2. Output이 catagory인 경우  
   - Classification Loss  
   - Cross Entropy  

## 03. 피어 세션  
멘토님께 여쭤 볼 BERT 논문 질문 리스트 정리하기 및 우리가 해결 할 수 있는 부분 해결하기  
오전 : GIT 연결해, branch 파기 (대회 서버와 git 연동)  

## 학습 회고  
이번주는 구인구팀세션을 진행하느라 한 주가 다 가버린 것 같다.  
그래서 지체되어 버린 학습 진도를 빨리 빼야 겠다는 생각이 들었다.   