---
title: "Day 040"
date: 2023-04-28

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---
{:.lead}

- Table of Contents
{:toc .large-only}
## 00. 데일리 스크럼  
노션에 기록  

- [x]  (7강) Model Serving
- [x]  Aistages 서버에서 다운 못 받은 것 확인
- [x]  과제 코드 제출
- [x]  (8강) 머신러닝 프로젝트 라이프 사이클
- [x]  (특강) AI Ethics - 오혜연
- [x]  주간 회고 작성
- [x]  주간 피드백 제출
- [x]  남은 특강들


---

## 01. 강의 정리 (서비스 개발 기초)  
&emsp;

Docker 실습, Streamlit 실습 등 수 많은 에러들을 해결하느라 듣지 못했던 남은 강의 모두 진행하였다.  


## 02. Streamlit 실습 완료!!  
&emsp;  

결국 새벽이 다 되어서야 완성한 실습이었다. 해결 방법은 GPU에서 만든 모델을 CPU에서 돌리고자 하니까 에러가 발생했던 것이었다.  
이에 관한 코드는 [↪️Link](https://forbuds.github.io/study/ml-dl/2023-04-28-How-to-load-DL-model-on-CPU-device/)에 정리해 두었다.  
제출 후에 조금씩 다듬느라 시간이 오래 걸렸지만 처음으로 딥러닝 모델을 가지고 만든 프로토타입이라 너무 재미있었다.  
&emsp;  
✅ 다음은 [Korean-specific ELECTRA model](https://huggingface.co/snunlp/KR-ELECTRA-discriminator)을 가지고 <span style="color: #e54685;background-color:#ffdce0">**Semantic Text Similarity(STS : 문장 유사도)**</span>를 계산한 결과를 [Streamlit](https://streamlit.io/)을 사용해 디스플레이한 모습이다.  
&emsp; → Streamlit 기본 예제는 [↪️Link](https://docs.streamlit.io/)에서 확인할 수 있다.   
&emsp; → [↪️ 변성윤 마스터님의 Streamlit 예제 정리](https://zzsza.github.io/mlops/2021/02/07/python-streamlit-dashboard/)

- 두 개의 문장을 입력하면
<span style="color: #e54685;background-color:#ffdce0">**0~5**</span>의 점수로 **유사도 점수**를 산출한다.  
- 0에 가까울수록 유사하지 않은 문장이고, 5에 가까울수록 유사한 문장이다.  
- 유사한 문장, 유사하지 않은 문장의 기준은 3점이다.
- 두 개의 예제로 실습을 진행하였다. 
  - <U>오늘 하루도 미소지으며 시작해요!</U> & <U>진짜 환하게 웃으면서 오늘 하루를 시작해 보아요!</U>  
  - <U>오늘 하루도 미소지으며 시작해요!</U> & <U>오늘은 날씨가 좋지 않아요.</U>  

![800x400](\assets\streamlit STS example.gif "streamlit STS example")

<span style="color: #848484">Streamlit 예제로 프로토타입을 만들어 [Record a screencast] 기능을 이용해 레코딩을 하면 .webn 형식의 동영상이 추출된다. 
이를 [cloudconvert](https://cloudconvert.com/webm-to-gif)라는 사이트의 webn to gif 기능을 이용하여 Gif 포멧으로 변환해 업로드 하였다!  
</span>

---


## 03. 학습 회고  
&emsp;   

결국 문제는 "모델을 어디에서 돌리냐"였는데, 그 오류를 해결하기까지 너무나도 오래 걸렸다.  
Klue relation extraction이 다음 대회로 예정되어 있으니 미리 예습해야겠다.  

  
---  

