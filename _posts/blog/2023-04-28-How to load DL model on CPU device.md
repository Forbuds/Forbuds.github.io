---
layout: post
title: How to load model.pt on CPU device

description: >
  GPU로 학습시킨 모델을 CPU로 불러오는 방법입니다.
sitemap: false
---


{:.lead}



- Table of Contents
{:toc .large-only}

## 문법 (Grammer)

`(model = torch.load('model.pt', map_location=lambda storage, loc: storage))
```
model = torch.load('model.pt', map_location=lambda storage, loc: storage)
```
 
## 설명 (Description)

Pytorch 공식 문서 [TORCH.LOAD](https://pytorch.org/docs/stable/generated/torch.load.html#:~:text=%23%20Load%20all%20tensors%20onto%20the%20CPU%2C%20using%20a%20function%0A%3E%3E%3E%20torch.load(%27tensors.pt%27%2C%20map_location%3Dlambda%20storage%2C%20loc%3A%20storage)) 부분을 살펴 보면 예제가 나와있다.   

"Example > Load all tensors onto the CPU, using a function"  

한참을 적용 못하고 MS bing에 물어봤더니 답변을 환상적으로 해 줬다!  
정말이지 자연어 처리 기술은 어디까지 발전할 것인가 기대되면서 무섭기도 하다.ㅎㅎ  
 
## Logs

```
torch.save(model, folder_name+ 'model.pt')   # save code
```
이렇게 저장한 모델을 불러오고 싶을 때 같은 GPU 였다면
```
model = CustomModel()
model = torch.load(log_dir+'model.pt')  # Prediction on GPU
```
이렇게 불러오면 됐지만, 모델을 서버에서 다운받아 CPU에서 처리해 개발하고 싶을 경우 (ex: windows) 다음과 같이 불러와야 한다.

```
model = CustomModel()
model = torch.load(log_dir+'model.pt', map_location=lambda storage, loc: storage)  # Prediction on CPU
```




