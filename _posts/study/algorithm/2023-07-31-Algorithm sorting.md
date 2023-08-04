---
layout: post
title: 정렬 - 이코테 내용
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
## 1. 선택 정렬 (n²)
`선택` 해 두고 정렬되지 않은 `나머지` 중에 최소값이나 최대값을 `선택` 해서 바꿔치기(`교환`)

탐색 범위는 반복할 때마다 줄어들게 되고, 매번 남은 탐색 범위 만큼 `데이터를 하나씩 확인`해서 가장 작은 데이터를 찾아감

매번 선형 탐색을 수행하는 것과 동일하다.

➡️ O(n²)인 이유

`이중 반복문`을 이용해서 구현할 수 있다, 그런데, python에서는 ` `c_i = l.index(min(l[i+1:]))` `이 가장 빠르다. 어차피 min도 선형 탐색이라 똑같다고 보면 된다. 대신 좀 빠름

다음은 위키피디아의 설명이다.

```
Worst complexity: n²
Average complexity: n²
Best complexity: n²
Space complexity: 1
Method: Selection
Stable: No
Class: Comparison sort
```

- [알고리즘 수업 - 선택 정렬 1](https://www.acmicpc.net/problem/23881)
- [수 정렬하기](https://www.acmicpc.net/problem/2750)
    - [설명 블로그](https://joylee-developer.tistory.com/91)    
    - 힌트: 시간 복잡도가 O(n²)인 정렬 알고리즘으로 풀 수 있습니다. 예를 들면 삽입 정렬, 거품 정렬, 선택 정렬
        <details>
        <summary>코드</summary>
        <div markdown="1">

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
        </div>
        </details>
