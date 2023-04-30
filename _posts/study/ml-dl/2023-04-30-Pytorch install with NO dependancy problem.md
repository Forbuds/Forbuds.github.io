---
layout: post
title: How install Pytorch with NO dependancy problem

description: >
  Pytorh를 의존성 문제 없이 설치하는 방법입니다. 
categories:
    - study
    - ml-dl
tags: [pytorch_tips]
sitemap: false
---


{:.lead}



- Table of Contents
{:toc .large-only}

## 출처 
- [Pytorch Docs](https://pytorch.org/get-started/pytorch-2.0/#requirements)
- In **"REQUIREMENTS"** part, you can see the code.

## 
- For CPU
 
  ```
  pip3 install numpy --pre torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/nightly/cpu
  ```
- For GPU ( if CUDA 11.8 )
 
  ```
  pip3 install numpy --pre torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/nightly/cu118
  ```




