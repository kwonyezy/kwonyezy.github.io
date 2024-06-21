---
title: "Goat Counter로 방문자 수 집계"
tags:
    - Writing Manual
    - 게시 가이드
date: "2024-02-02"
thumbnail: "https://i.ibb.co/xj20N3N/card.webp"
bookmark: true
---

[![goatcounter](https://cdn.icon-icons.com/icons2/2699/PNG/512/goatcounter_logo_icon_170078.png){:class="img-md"}](https://www.goatcounter.com/)

GoatCounter는 무료 기부 지원 호스팅 서비스 또는 자체 호스팅 앱으로 제공되는 오픈 소스 **웹 분석 플랫폼** 
이 플랫폼은 Google Analytics나 Matomo의 대안으로서 사용하기 쉽고 의미 있는 개인정보 보호 친화적인 웹 분석을 제공하는 것이 목표
(*공식 가이드 참고*)

# 시작하기
---

## 1. 가입하고 액세스 코드 받기

[여기](https://www.goatcounter.com/signup) 에서 계정 생성
`https://[my-code].goatcounter.com` 에서 블로그 통계에 액세스 가능

## 2. `_config.yml`에 코드 추가

```
goatcounter_code: [my-code]
```
(페이지 조회수가 전혀 표시되지 않으면 광고 차단기가 GoatCounter를 차단하고 있는지 확인)


## 3. 방문자 카운터 허용

**Goat counter** 에 로그인 한 후 [Settings](https://[my-code].goatcounter.com/settings/main) 탭으로 들어가기

`Allow adding visitor counts on your website` 가 선택되어있는 지 확인하기

![](https://i.ibb.co/R7TKCmy/2024-01-13-043651.png){:class="img-md"}
