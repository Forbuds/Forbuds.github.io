---
title: "Day 030"
date: 2023-04-14

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크럼  
노션에 기록
- [x]  강의 N2N
- [x]  강의 N2M
- [ ]  강의 Prediction Service

---

- [x]  코드 다운 미리
- [x]  강의 미리 다 들어두기
- [x]  회고록 작성
- [ ]  스페셜미션
- [ ]  (3-2강-실습) N21 Sentence Classification.ipynb 코드 다시 뜯어볼 것
- [x]  Wandb 는 쓸 줄 알아야겠다!


## 01. BERT 논문 요약 마무리
---    
      

 

## 02. 강의 정리  

N2N problem  
 - 예제  
  
     POS : part별로 뜯어내줌  (part of speech tagging, 형태소 분석)  
    Name : segment한 다음, type부여   (named Entitiy Recognition, 개체명 추출)  

 - loss : CE  (입력, 출력, 정답 모두 N개의 토큰을 가지고, N개의 토큰별로 POS개수만큼)  

N2M problem
  - [인코더] → context vector → [디코더]  

    디코더가 그때그때 필요한 말을 여러 번에 걸쳐서 생성해 낸다.  
  - 원리  
     
    중요한 부분들이 인코더를 통해서 벡터 스페이스의 벡터로 표현된다  
    벡터 스페이스에 올라와 있는 여러 벡터들 중에 어떤걸 활용할찌 그때그때 선택한다  
    N번에 걸쳐 매 step마다 encoder가 만들어 놓은  벡터 스페이스에서 매번 추려 낸다  
  - Example  
    - 번역 문제, 품사 태깅 문제 (한국어 같은 경우 N2M), 질의 응답(챗봇 등), 이미지 태깅  
  - Decoding strategy  
    - searching 방법에 완탐, beam search, greedy 등이 있음  
    - 개선 : N-gram, Sampling(random, top-k, top-p)  

Wandb 세팅  
- 도움이 되었던 [블로그](https://pebpung.github.io/wandb/2021/10/06/WandB-1.html)  
- [공식 페이지](https://wandb.ai/site) : https://wandb.ai/site  
  
---

## 03. 멘토링 세션 
9시 시작  
- 조교님 인턴중 느낀 점  
    
    코테 진짜 열심히. 하지 않는다면 지금까지 열심히 해 왔던 것을 말할 기회를 놓친다.  
    작은 에러나 시행착오 하나하나를 정말 잘 기록하고넘어가야겠다.  
    it쪽으로 오고 싶으면 it에서 해보는 것 추천 *인턴이라도  
    추천? 가고 싶은 회사의 요구 사항을 꼭 봐야 한다.  
    공고들이 뭘 하고 있는가 (기본사항은 무조건 채우고 우대사항중에 마음에 드는거 디벨롭)  
- 네이버 부스트캠프 대회 관련 실험 기준  
  - 풀러로 조절해 보는 것 추천 * CLS 토큰을 사용해서 classification 하는 task가 일반적인데,
나오는 토큰 중 max를 뽑아내거나 avg 하는 방법이 있다. pooler로 조절해 볼 수 있으니 찾아볼 것.  
  - augmentation 방법을 고민 많이 해 볼 것  
  - validation 뜯어볼 것  
  - 피어슨은 모호한걸 잘 못맞추는 경향이 강한 지표이다. 그렇다면 쉬운건 확실하게 맞추게 하고 나머지 가지고 하는 방법을 취하는 것도 좋은 방법일지도?  
  - encoder 종류 : corss encoder(klue, roberta-large), dual encoder  
  
---  

## 04. 주간 학습 회고  
  
  

**잘했던/좋았던/계속할 것**  

- 구인구팀 열심히 한 것. (팀 구성 완료)  
- aistages 서버를 vscode로 띄우고, github와 연결한 것.  
- baseline code 제출한 것  

**잘못한/아쉬운/부족한 것→개선방향**  

- 강의를 다 듣지 못하였다. → 주말까지 마무리 할 것  
- 한솔이가 떠났다 😭  

**도전/시도할 것**  
 
- baseline코드 미션을 통해서 향상시키기  

**키워드(공부한/알게된/느낀 점)**  

- NLP 트랙에 잘하는 분들이 정말 많은 것 같다. 다 다양한 분야!  