---
title: "Giscus로 블로그 댓글 관리"
tags:
    - Writing Manual
    - 게시 가이드
date: "2024-02-03"
thumbnail: "https://i.ibb.co/V9j2Qsg/giscus-Wl0-X3byd-az-U68-1.webp"
bookmark: true
---

* 해당 글은 단순 게시글 가이드용이며, 기존 테마 (https://github.com/byanko55/jekyll-theme-satellite)에 게재된 글을 변형하였습니다.

[![goatcounter](https://opengraph.githubassets.com/4f866d5b634e7cd5422af77f8dbfb6d48dd288b7c5c18326544c1973210320ed/giscus/giscus){:class="img-lg"}](https://www.goatcounter.com/)

**Giscus** 는 자체 DB 없이 운영되는 **무료 댓글 시스템**
Giscus는 GitHub Discussions를 사용하여 선택한 매핑(URL, 경로 이름, 제목 등)에 따라 관련 댓글을 저장하고 불러옴

방문자가 댓글을 달기 위해서는 GitHub OAut 통해 giscus 앱이 그들의 대신 게시할 수 있도록 승인해야 하며, 
방문자가 GitHub Discussion에 직접 댓글을 달 수도 있고, 댓글은 GitHub에서 관리 가능

# 전제 조건
---

## 1. github 저장소 만들기

웹 사이트 호스팅에 *GitHub Pages* 를 사용할 예정이라면 해당 저장소 (i.e., `[userID].github.io`) 를 선택 가능

**public** 방문자가 토론을 볼 수 있도록 하려면 repository는 **public** 으로 지정


## 2. 토론 기능 켜기

GitHub 저장소 설정에서 `General` > `Features` > `Discussions`  기능이 활성화되어 있는지 확인

![Discussion](https://i.ibb.co/P1FV02D/giscus-00.png)


# Giscus API 활성화
---

\* [Configuration guide](https://giscus.app/) 를 참고하여 단계별로 진행

![Verification](https://i.ibb.co/y87w8rB/giscus-02.png)

다음 매뉴얼 페이지에서 아래로 스크롤하여 `Discussion Category` 옵션을 선택
(다른 옵션은 별도 선택 불필요)

![Verification](https://i.ibb.co/0hqLWX0/giscus-03.png)

## 1. `_config.yml` 복사

giscus script를 얻었으며, 아래에 표시된 것처럼 빨간 상자로 표시된 네 가지 속성을 복사

![](https://i.ibb.co/Z154x8P/giscus-04.png)

그 값을 루트 디렉터리에 있는 `_config.yml` 에 붙여넣기

```
# External API
giscus_repo: "[ENTER REPO HERE]"
giscus_repoId: "[ENTER REPO ID HERE]"
giscus_category: "[ENTER CATEGORY NAME HERE]"
giscus_categoryId: "[ENTER CATEGORY ID HERE]"
```
