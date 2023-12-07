---
layout: post
title: 그래프 - 상길북 내용
description: >
  다시 시작하는 알고리즘 공부
categories:
  - study
  - algorithm

sitemap: false
---


{:.lead}



- Table of Contents
{:toc .large-only}
# 오일러 경로와 헤밀턴 경로
## 오일러 경로
간선의 차수가 짝수면 한 붓 그리기 가능하다.
간선을 한 번씩 모두 방문
## 헤밀턴 경로
정점을 한 번씩 모두 방문
- 헤밀턴 순환 : 출발점으로 돌아옴
  - 외판원 문제
    - 헤밀턴 순환으로 해결 가능
    - 각 도시를 방문하고 돌아오는 가장 짧은 경로 찾기 문제
    - DP를 쓰면 최적화 가능 O($n^2  2^n$)

# DFS, BFS
## 쓰임새와 차이
### DFS
- 구현 방법: `스텍` / `재귀`
- `백트레킹에` 자주 쓰임
  - 범위는 백트래킹⊃DFS
    - 백트래킹이 DFS보다 좀 더 넒은 의미를 가진다.
  - 백트래킹은 주로 재귀로 구현
### BFS

- 구현 방법: `큐` - deque 자료형 이용
  - 📌 BFS는 절대 재귀로 풀 수 없다.
- 최단경로에 자주 쓰임 - `다익스트라`
## DFS
## BFS

```python
        import sys
        input = sys.stdin.readline

        n = int(input())
        l = [int(input()) for _ in range(n)]
        # print(n,l)

        for i in range(n-1):                        # 마지막 인덱스 직전까지 탐색
            g = l[i]                                # 현재 값 보관  -> 항상 보관은 하나만 하면 된다.
            c_i = l.index(min(l[i+1:]))             # i+1 부터 끝까지 중에 가장 작은 인덱스 추출    -> list는 역시 내장 함수가 가장 빠르다
            if g <= l[c_i]:
                pass
            else:
                l[i] = l[c_i]
                l[c_i] = g
        print('\n'.join([str(i) for i in l]))
        ```
