---
layout: post
title: GLUE Benchmark란?

description: >
  GLUE Benchmark에 대해 정리해 두었습니다.
categories:
    - study
    - ml-dl
tags: [papers,nlp]
sitemap: false
---


{:.lead}



- Table of Contents
* toc
{:toc .large-only}

## 자료 및 링크 ( 논문, hugging face..)

    
  - [GLUE 논문](https://openreview.net/pdf?id=rJ4km2R5t7)
  
  - [GLUE Benchmark](https://gluebenchmark.com/)
    
  - [mariosasko/glue · Datasets at Hugging Face](https://huggingface.co/datasets/mariosasko/glue)
    
  - [Papers with Code - GLUE Dataset](https://paperswithcode.com/dataset/glue)
    
## GLUE란?
- "자연어 처리 task들의 종합적인 성능을 평가하는 지표"의 역할을 하는 dataset이다.

## GLUE를 사용하는 이유?
- Pretrained 모델의 등장으로 모델의 일반적인 성능을 평가할 지표가 필요해 졌기 때문이다.
  


[NLP 이해하기](https://hryang06.github.io/nlp/NLP/#snlistanford-natural-language-interence-corpus)

[NLP Task 맛보기 - (2) NLU, QA](https://only-wanna.tistory.com/entry/NLP-Task-맛보기-2-Question-AnsweringQA)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5819f2bd-a917-4b5a-b0b4-86c1816ee79a/Untitled.png)

## 표로 정리
    
  - [출처](https://docs.google.com/spreadsheets/d/1BrOdjJgky7FfeiwC_VDURZuRPUFUAz_jfczPPT35P00/edit#gid=0)
   

| Corpus | 문장 개수  | task | metrics | label | size (train/dev/test) |
| --- | --- | --- | --- | --- | --- |
| CoLA | 1 | acceptability | Matthews corr. | 0 / 1
acceptable / not acceptable | 10K / 1K / 1.1K |
| SST-2 | 1 | sentiment | acc. | (0~1) negative~positive | 67K / 872 / 1.8K |
| MRPC | 2 | paraphrase | acc. / F1 | 0 / 1
same / not same | 1.7K / 408 / 3.6K |
| QQP | 2 | paraphrase | acc. / F1 | 0 / 1
same / not same | 400K / - / 391K |
| STS-B | 2 | sentence similarity | Pearson/Spearman corr. | 1 ~ 5 
(similarity score) | 7K / 1.5K / 1.4K |
| MNLI | 2 | NLI | metched acc. / mismatched acc. | 0 / 1 / 2    *(e/n/c) entailment , contradiction , neutral | 393K / 20K / 20K |
| QNLI | 2 | QA/NLI | acc. | 0 / 1    answerable, not answerable entailment , not entailment | ? 105K / 5463 / |
| RTE | 2 | NLI | acc. | entailment / not entailment | 2.7K / - / 3K |
| WNLI |  | coreference/NLI | acc. |  | 706 / - / 146 |

## Task 별 정리
- NLI :

  자연어 추론 문제 (inference) 란, 두 문장이 주어졌을 때, 하나의 문장이 다른 문장과 논리적으로 어떤 관계에 있는지를 분류하는 것입니다. 유형으로는 모순 관계(contradiction), 함의 관계(entailment), 중립 관계(neutral)가 있습니다.

  - gpt
      
      주어진 전제문장(premise)과 가설문장(hypothesis)에서, 전제문장이 가설문장을 포함(entail)하거나 가설문장이 전제문장과 모순되는(contradict) 경우 또는 두 문장이 상호작용하지 않는(neutral) 경우를 예측하는 것이 과제입니다. 이러한 작업은 자연어 처리 분야에서 자연어 추론(natural language inference)이라고 불립니다. 주로 **자연어 이해, 기계번역, 질의응답** 시스템 등에서 활용됩니다.
      
  - entail 어떤 의미?
      
      "Entail"의 한글 뜻은 "수반하다", "의미하다"입니다. NLI나 RTE와 같은 자연어처리 분야에서는 "전제 문장이 주어졌을 때 가설 문장이 수반되는지 여부"를 판단하는 과제를 의미합니다.
    

- **CoLA** 

  - The Corpus of Linguistic Acceptability
  - 문법적으로 맞는지 bin

- **SST-2**

  - The Stanford Sentiment Treebank
  - 영화 리뷰에서  negativity(0) ~ positivity(1)

- **MRPC** 

  - Microsoft Research Paraphrase Corpus
  - 페러프레이징 잘 되었는지

- **QQP** 

  - Quora Question Pairs is a binary classification
  - 두 질문 간 유사여부

- **STS-B** 

  - The Semantic Textual Similarity Benchmark
  - 문장간 유사도

- **MNLI** 

  - Multi-Genre Natural Language Inference
  - premise 문장들은 말로 된 대화(transcribed speech), 인기있는 소설(popular fiction)과 정부 보고서(government reports) 등 다양한 출처에서 수집된다.
  - 테스트 셋은 matched와 mismatched로 구성되며, matched는 학습 셋과 같은 출처에서 가져온 데이터이고, mismatched는 다른 출처에서 가져온 데이터로서 도메인 전이를 필요로 한다.  ?
  - 예시
      - 첫번째 예시:
          - 가정문: 'Jon walked back to the town to the smithy.'
          - 추론문: 'Jon traveled back to his hometown.'
          - 예측결과: 1 (중립)
          - 이유: 두 문장은 내용이 유사하지만, 'town'과 'hometown'이 조금 다르기 때문에 정확한 추론을 하기 어렵습니다. 따라서 중립으로 판단됩니다.
      - 두번째 예시:
          - 가정문: 'Tourist Information offices can be very helpful.'
          - 추론문: 'Tourist Information offices are never of any help.'
          - 예측결과: 2 (모순)
          - 이유: 가정문과 추론문이 반대의 의미를 가지고 있기 때문에, 모순으로 판단됩니다.
      - 세번째 예시:
          - 가정문: "I'm confused."
          - 추론문: 'Not all of it is very clear to me.'
          - 예측결과: 0 (추론 가능)
          - 이유: 가정문과 추론문은 서로 반대되는 내용을 담고 있지 않으며, 가정문에서 드러난 감정을 고려할 때 추론 가능한 내용이라고 판단됩니다.

- **QNLI** 

  - Question Natural Language Inference
  - Question Answering / Natural Language Inference
  - The Stanford Question Answering Dataset
      - 기계독해
      - 스탠포드 질의응답 데이터셋(SQuAD)은 질문-문단 쌍으로 구성된 질문응답 데이터셋으로, 해당 문단에서(위키피디아에서 추출) 질문에 대한 답변을 포함하는 문장이 하나 포함됩니다
  - 예시
      
      ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/113b1138-8f3e-420f-bb59-3697a97dc8ce/Untitled.png)
    

- **RTE** 

  - Recognizing Textual Entailment
  - 여러 온라인 뉴스 소스를 모은 데이터, 작업은 premise가 hypothesis를 [entail](https://www.notion.so/GLUE-Benchmark-7527653d71f04a90891e7e958918719a)하는지 예측하는 것입니다.
  - 예시
      
      ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/60c0540d-55cc-480a-b53d-264c6d1a0514/Untitled.png)
    

- **WNLI** 

  - Winograd NLI
  - [https://cs.nyu.edu/~davise/papers/WinogradSchemas/WS.html](https://cs.nyu.edu/~davise/papers/WinogradSchemas/WS.html)
  - Coreference : 대명사가 어떤 명사를 가르키는지
      - The trophy doesn't fit into the brown suitcase because it's too [small/large].
          
          What is too [small/large]?
          
          **Answers:**The suitcase/the trophy.
        
- **NLI**
    - 예시
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edc3cf25-5ad9-4ca5-ae58-1030e17857b0/Untitled.png)