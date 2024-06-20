---
title: "블로그 게시 가이드"
tags:
    - Writing Manual
    - 게시 가이드
date: "2024-02-04"
thumbnail: "/assets/img/thumbnail/sample.png"
bookmark: true
---

* 해당 글은 단순 게시글 가이드용이며, 기존 테마 (https://github.com/byanko55/jekyll-theme-satellite)에 게재된 글을 변형하였습니다.

사이트에 게시물을 작성하고 게시하는 방법에 대한 단계별 프로세스

# `_pages` 디렉터리 생성
---
`_pages` 루트가 없으면 해당 이름의 디렉터리 생성

```
$ mkdir _pages
$ cd _pages
```

git hub 웹사이트에서는 `_pages` 이름으로 Add file

# 디렉터리 구조 구성
---
해당 테마는 계층적 디렉토리 구조를 제공

```txt
._pages
├── Category A
├── Category B
|   ├── Subcatecory b
|   ├── Subcatecory c
```

## `index.md` 필수 생성

모든 폴더 생성 시 `index.md` 를 아래와 같이 두 개의 점선으로 구성하여
폴더 생성 후 가장 최우선으로, 필수적으로 생성

```
---
---
```

또는 각 디렉터리에서 다음 명령을 입력 가능

```
$ echo -e "---\n---" > index.md
```

각 폴더별 `index.md` 가 추가된 `_pages` 의 구조

```txt
._pages
└── index.md
├── Category A
|   └── index.md
├── Category B
|   └── index.md
|   ├── Subcatecory b
|       └── index.md
|   ├── Subcatecory c
|       └── index.md
```

# 블로그 게시글 작성
---

`.md` 파일 확장자를 사용하여 게시글을 작성 (예시 : *Post-name.md*)

모든 블로그 게시글 파일은 제목이나 기타 메타데이터를 설정하는 데 사용되는 머리말로 시작해야 함

**`title` 과 `date` 필드는 필수적으로 작성해야 함.** 

```
---
title: "Example Post"
date: "2023-12-01"
---

# Welcome

**Hello world**, this is my first Jekyll blog post.

I hope you like it!
```

## 게시글 썸네일 이미지 설정

`thumbnail` 렌더링 시 대표 이미지를 표시하려는 게시물에 속성을 추가

```
---
title: "Example Post: thumbnail exists"
date: "2023-12-02"
thumbnail: "/assets/img/thumbnail/bricks.webp"
---
```

![](https://i.ibb.co/T8Rsb6L/21312.webp){:class="img-lg"}

## 카테고리 태그

관련 게시물을 검색하거나 페이지 하단에 고정하고 싶을 때 유용

```
---
title: "Classic Literature #1: Romeo and Juliet"
tags:
    - book
    - epic novel
    - romance
date: "2023-12-04"
thumbnail: "/assets/img/thumbnail/nightgardenflower.jpg"
---
```

![](https://i.ibb.co/LDKJC7p/1231.webp){:class="img-lg"}

Note that the `tags` attribute won't be reflected to the sidebar navigation.

## 북마크

`bookmark: true` 로 설정하면 목차에 해당 게시글이 표시

```
---
title: "Markdown from A to Z"
tags:
    - user manual
    - markdown
    - writing format
date: "2023-09-05"
thumbnail: "https://i.ibb.co/MRzw6T9/sample.webp"
bookmark: true
---
```

![](https://i.ibb.co/2sFZNNK/21313.webp){:class="img-sm"}

# `_pages` 구조
---

```txt
._pages
└── index.md
└── markdown guide.md
├── License
|   └── index.md
|   ├── 네트워크관리사
|       └── index.md
|       └── TCP-IP.md
|       └── 기타 프로토콜.md
├── Portfolio
|   └── index.md
|   └── Introduce.md
├── Writing Manual
|   └── index.md
|   ├── Guide
|       └── index.md
|       └── Posting Guide.md
|       └── Markdown Guide.md
|       └── Comment System.md
|       └── Vistor counter.md
|   ├── example
|       └── index.md
|       └── example_01.md
|       └── example_02.md
```
