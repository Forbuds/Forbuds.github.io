---
title: "Day 039"
date: 2023-04-27

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

- [x]  (6강) MLOps 개론
- [x]  EDA 추가 (오전)
- [x]  (9강) 웹 서비스 형태 - Streamlit
- [ ]  (9강 실습) 웹 서비스 형태
- [ ]  (특강) 내가 만든 AI 모델은 합법일까, 불법일까 (문지형)
- [x]  Wrapup 어투맞추기
- [x]  조교님한테 받고 싶은 피드백 작성


---
## 01. 오류 해결 일지  
- Python 버전별 관리 가능하도록 두기  [↪️ Notion에 간단 정리](https://glacier-fiction-d9a.notion.site/Python-550f87ca241244d1bbe33f605eab90ca)
  - 혹시나 안되는 이유가 python의 버전에 있을지도 모르겠다는 생각에 python 버전별 관리를 해 두었다. (Streamlit 실습을 진행하기 위해서 torch를 쓰기 때문에 환경별 관리가 필요해 가상환경을 만들어 진행하였기 때문!)
- 계속해서 PS와 cmd에서 python 명령어나 pip 명령어가 자꾸만 오류가 났다.  
  - 'pip'은(는) 내부 또는 외부 명령, 실행할 수 있는 프로그램, 또는 배치 파일이 아닙니다.  
  - 종료했다가 다시 켜니까 동작했다. 혹은 관리자 권한으로도 시도해 보자.  
- Pytorch는 항상 이런 식으로 설치해야 의존성 문제가 없는 듯 하다. [↪️ Link](https://forbuds.github.io/study/ml-dl/2023-04-30-Pytorch-install-with-NO-dependancy-problem/)
  - 현재는 cpu 버전이라 다음과 같은 코드로 작성해줬다.
  
    ```
    pip3 install numpy --pre torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/nightly/cpu
    ```
- 오류를 하도 쳐다보고 있자니 결국 머리가 굳어
  - AttributeError: module 'main' has no attribute 'Model' 다음과 같은 에러도 만났다.
  - Model을 정의하고 model.pt를 불러와야 하는데 그걸 빼먹은 것. 정말 바보같았다. ㅎㅎ..

## 02. 학습 회고  
&emsp;   

✅ 다 잘 되었다면 재시작해보면 적용될 때도 많으니 항상 고려할 것! 
- 계속해서 설치했는데 적용이 안되었다면, 관리자 모드 혹은 재시작을 무조건 고려해볼 것.

✅ 그래도 오류 해결 일지나, 설치 로그를 만들어 두니 어떤 과정을 수행하고 있고, 지금까지 어떤 오류들을 만났는지 확인할 수 있어 다시 처음부터 시작할 때 빠르게 적용이 가능했다!!
- 이번 주의 잘한 점 :)
  
---  

