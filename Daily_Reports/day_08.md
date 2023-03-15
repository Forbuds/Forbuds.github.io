---
title: "Day 008"
date: 2023-03-15

categories:
  - Blog
tags:
  - [Boostcamp, up-stage]
toc: true
toc_sticky: true
---

## 00. 데일리 스크럼
노션에 기록
- [ ]  Pytorch 4~6 (40 5/ 6x)
- [x]  기본과제 1 완료
- [x]  기본과제 2 시작

<span style="background-color:#ffdce0">Convolution</span>
## 01. Course
**4-5강**  
들음
정리하는 중


## 02. 멘토링 세션

**멘토링 질문**  

- 트랜스포머보다 먼저 읽으면 도움이 되는 논문 하나만 추천해주실 수 있을까요?  
- 자연어 처리 기초를 설명해 주는 블로그나 영상 또는 책 추천 가능할까요?  
    - [김기현의 자연어 처리 딥러닝 캠프 파이토치 편](http://www.yes24.com/Product/Goods/74802622)  
    - [트랜스포머를 활용한 자연어 처리](http://www.yes24.com/Product/Goods/115633781)
    - [ratsgo.github](https://ratsgo.github.io/)  
    - [한국어 임베딩](https://github.com/ratsgo/embedding)  
    - [고려대학교 산업경영공학부 DSBA 연구실 Youtube](https://www.youtube.com/watch?v=UInnl60pzkA&list=PLetSlH8YjIfVzHuSXtG4jAC2zbEAErXWm&ab_channel=%EA%B3%A0%EB%A0%A4%EB%8C%80%ED%95%99%EA%B5%90%EC%82%B0%EC%97%85%EA%B2%BD%EC%98%81%EA%B3%B5%ED%95%99%EB%B6%80DSBA%EC%97%B0%EA%B5%AC%EC%8B%A4)  
    - [논문 템플릿](https://www.notion.so/yukyunglee/Template-171be90cfbc947d3b28f28e0bd4d026b?pvs=4)  
- [https://sanghyu.tistory.com/85](https://sanghyu.tistory.com/85) : 모델 만들때, cat() 과 stack() 적용해 주는 경우가 많습니다. 각각 어떤 상황에서 쓰여지는 지 알 수 있을까요? cat과 달리 stack은 차원을 더해서 붙여 주는 것 까지는 이해 했고, 코드 상으로도 이해 했습니다. 하지만 각각을 어떤 기능을 부여해주고 싶을 때 사용하는지 궁금합니다!  
    - 스택은 룩업 테이블로, 컨캣은 멀티모달로 이해하면 직관적임  
    - 스택은 특징을 살려서 버티컬 하게, 컨캣은 최종 하나의 피쳐를 뽑아 내는 것으로 이해  
- 논문 읽는 법  
    - 초록을 읽고 흐름 예상  
    - 내 가설과 논문의 포인트가 실제로 얼만큼 매칭되는지 확인하면서 읽는다  
    - 논문 디테일을 이해한다  
    - 코드와 매칭해 본다.  
    - *method - 텍스트로 이해가 되지 않으면 코드를 보는 습관도 좋음  
    - *result - 이 실험을 통해서 어떤 효과를 입증한 거지? 고민하기  
- 그 외 팁  
    1. 코딩과 개념 사이의 밸런스 :  day1 코딩 day2 개념 이런 방식  
    2. 개념은 어느 정도까지 알아야 할까요? 경사 하강법과 같은 기초 지식은 자세히, pytorch 기초와 같은 부분은 사용해보고 넘어가는 형식  

## 03. 과제 수행 과정/과제 결과물에 대한 정리
- 기본( 커스텀 모델 제작) : pytorch 사용법 익히기  완료

## 04. 학습 회고
- pytorch에 대한전반적인 문법을 학습하였다.