---
title: "Day 024"
date: 2023-04-06

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크럼  
노션에 기록

- [x]  오전 - BERT 질문 생각하기  
- [ ]  기본과제 3,4 끝내기 (마지막 부분 못함)
- [x]  9강 실습 (transformer 사용해보기)
- [x]  10강 실습
- [x]  강의 모두 듣고 정리하기 (다 들었지만 정리는 못함!)
- [x]  구인구팀 작성
- [ ]  백준 1

   
## 01. BERT 영상 시청  
    
### BERT 모델은 기본적으로 사전 학습 후 fine tuning하는 방식으로 작동된다.  
### 사전 학습된 언어 모델 사용 (pre-training + fine tuning )  
  

---  
    

😭 먼저, 임베딩을 사용하는 **이전의** 방법 : **사전 훈련된 워드 임베딩**  

- 임베딩 층을 랜덤 초기화  
- 사전학습 임베딩 벡터  가져와 (Word2Vec)  

→ 벡터는 오직 **하나**! 단어당 두가지 의미를 가질 수도 있는데 이를 반영 x  


✅ [사전 훈련된 언어 모델](https://wikidocs.net/108730)  

- 먼저 LSTM을 학습한 후, 텍스트 분류 테스크로 파인 튜닝하는 방법..!  
- 이때 사전학습이란❓  
    - <이전 단어 ➡️ 다음 단어>  
    - 예측하는 학습을 진행.  
- 🔥장점 : 학습 전 사람이 별토 레이블을 지정해줄 필요가 없다.  

  
🔥 언어 모델을 사전 훈련하는 것으로 트렌트가 바뀜  

  

1. Semi-supervised Sequence Learning  
      - LSTM  
2. ELMo  
      - LSTM 양방향  
3. GPT-1  
      - Transformer
   

  ---
### BERT에서도 <span style="background-color:#ffdce0">사전 학습 모델</span>을 사용함. 
### 🔥 추가적으로 , <span style="background-color:#ffdce0">**Masked Language Model**이용</span>.
    

### 정리    
1. Input Representation    
    - Token embedding
      - WordPiece embeddings  
      - [CLS] classification embedding  
      - Packed sentence embedding [SEP]  
    - Learned positional embedding  
    - Segment Embedding  
2. Pre-training Tasks  
    - Masked LM  
    - Next Sentence Prediction  
3. 윗 단에 하나의 레이어만 걸쳐 두면 bert모델 위에 어떠한 task도 태울 수 있다.  

## 02. Peer session  
프로젝트 아이디어 공유  


## 03. 학습 회고  

