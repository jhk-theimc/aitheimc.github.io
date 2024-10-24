---
layout: post
title:  더아이엠씨 AI 블로그 post layer 작성법
date:   2024-10-18
author: Jin
excerpt_separator: "<!--more-->"
tags:
    - guide
    - markdown
    - rule
---

본 포스팅은 더아이엠씨 AI 블로그 작성을 위해 반드시 작성해야하는 layout 작성법을 서술하였습니다. 작성중인 마크다운 문서에 layout을 첫줄부터 입력한 후 본 글을 시작합니다.
<!--more-->

## layout 작성법
### 개요 및 작성 예시
작성한 그대로 보여지진 않지만 타이틀, 날짜, 저자 등 전면 정보를 테마에 적용된 룰을 준수하여 웹사이트에 표시 됩니다. 반드시 첫줄부터 작성해야 하며, 본 포스팅에 사용된 예시는 아래와 같습니다.

```md
---
layout: post
title:  더아이엠씨 AI 블로그 작성 간단 설명
date:   2024-10-18
author: Jin
excerpt_separator: "<!--more-->"
tags:
    - guide
    - markdown
    - rule
---
```

### 필수 레이아웃 기능 설명
#### layout, title, date
`layout`은 `post` 로 고정하여 작성된 문서가 `post` 룰을 따른다는 것을 반드시 알려주고, 문서에 대한 제목과 작성 날짜를 `title`과 `date` 항목에 아래와 같이 작성합니다. 

```md
---
layout: post
title: 더아이엠씨 AI 블로그 작성 간단 설명
date:   2024-10-18
----
```

#### author
본 테마는`_data/authors.yml` 에 작성된 작성자 정보를 불러와서 작성된 문서에 표시하는 기능을 제공합니다. 이를 위해 아래와 같이 작성합니다.

```md
---
author: Jin
---
```

만약, 신입사원이 입사하거나 기존 직원의 상태가 변경된다면 `_data/authors.yml` 에 신입사원 정보를 추가하거나, 수정 합니다. 예시 및 항목별 설명은 아래와 같습니다.
```
Jin: # key value
  name: Jin # 이름 및 별명
  picture: /images/jin/jin_profile.jpg # 프로필 사진
  description: R&M teamleader # 직무, 직책, 업무 등 자신이 원하는 설명 내용 작성
```

#### excerpt_separator
목차에 설명글로 표시되는 부분을 임으로 설정하는 기능을 제공하며, `"<!--more-->"` 등 구분자를 사용하면 구분자가 있는 위치까지만 목차에 표출 됩니다. 사용예시는 아래와 같습니다.

```md
---
excerpt_separator: "<!--more-->"
---
```

## [참고1] 마크다운 문서 작성시 참고 할 수 있는 사이트

olvimama 블로그(한글)
  
[https://olvimama.github.io/post/](https://olvimama.github.io/post/) # 웹사이트
[https://github.com/olvimama/olvimama.github.io/tree/master/_posts](https://github.com/olvimama/olvimama.github.io/tree/master/_posts) # 마크다운 코드

so-simple-theme 블로그(영문) 

[https://mmistakes.github.io/so-simple-theme/posts/](https://mmistakes.github.io/so-simple-theme/posts/) # 웹사이트
[https://github.com/mmistakes/so-simple-theme/tree/master/docs/_posts](https://github.com/mmistakes/so-simple-theme/tree/master/docs/_posts) # 마크다운 코드



## [참고2] 
미결정 현황 : tag와 catgories 기능이 있고 각 기능을 사용할지 사용한다면 어떤 목적으로 사용할지 등을 논의해야할 필요성이 있음