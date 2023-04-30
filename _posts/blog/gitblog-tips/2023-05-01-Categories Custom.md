---
layout: post
title: Gitblog custom - Categories Custom
description: >
  Gitblog의 categories를 관리하는 방법을 정리합니다.
categories:
  - blog
  - gitblog-tips
sitemap: false
---


{:.lead}


- Table of Contents
{:toc .large-only}



## Configure modify
--- 


_config.yaml

```bash
menu:
  - title:             Newcategory
    url:               /newcategory/
```

## Post files
--------------------------------------------------------------------------------
```
│
├─_featured_categories
│  │
│  └─newcategory.md
```
newcategory.md
```bash
---
layout: list
type: category
bigtitle: Newcategory
sitemap: true
hide_description: false
order: 1
description: >
  Blah~~
---
# Newcategory
```

## Post files

--------------------------------------------------------------------------------

_posts\newcategory\yyyy-mm-dd-Tag-d.md  (name이 00-00-이정도는 길어야 한다. 00.md로 끝나면 인식 못함
```bash
---
layout: post
title: Gitblog custom - test
description: >
  Gitblog에 Tag를 추가하는 방법을 정리합니다.
categories:
  - blog
  - daily-log
sitemap: false
---
```