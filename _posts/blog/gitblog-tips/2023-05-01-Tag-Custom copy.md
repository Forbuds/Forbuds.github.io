---
layout: post
title: Gitblog custom - Add tags
description: >
  Gitblog에 Tag를 추가하는 방법을 정리합니다.
categories:
  - blog
  - gitblog-tips
sitemap: false
---


{:.lead}


- Table of Contents
{:toc .large-only}

## Git blog의 tag 기능을 추가하였다!

### Configure modify
--- 
_config.yaml
```bash
collections:

  featured_tags:
    permalink:         /:name/
    output:            true
```
### Make tagename
--------------------------------------------------------------------------------

/_featured_tags/tagname.md
```bash
---
layout: list
title: tagname
slug:   tagname
hide_description: false
description: >
  blah..
---
# tagname
```
### In posts
--------------------------------------------------------------------------------

/_posts/yyyy-mm-dd-Title.md
```bash
tags: [tagname,tag2, ,,,]
```

---

## 부족한 점
sitemap을 클릭하면
- home/study/ml-dl
  - 404
- home/ml-dl
  - 정상적으로 나온다.


## 앞으로 구현할 Todo
- 이전/다음 포스트로 옮기는 기능
- Related posts를 현재 tag나 category로 한정시키는 방법


