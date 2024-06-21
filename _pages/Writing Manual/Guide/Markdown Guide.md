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

# 제목
---

단어나 구문 앞에 # 기호를 추가
#의 개수에 따라 강조의 차이가 있음

|Markdown|HTML|Rendered Output|
|---|---|---|
|\# Header 1|<h1>Header 1</h1>|<span class="sh1">Header 1</span>|
|\#\# Header 2|<h2>Header 2</h2>|<span class="sh2">Header 2</span>|
|\#\#\# Header 3|<h3>Header 3</h3>|<span class="sh3">Header 3</span>|

# 문자 속성
---
텍스트를 굵게 또는 기울임꼴로 만들어 강조를 추가


### Bold
<u>asterisks(*)를 두 개</u> 추가 (예시 : `**text**` = **text**) 
단어 중간을 굵게 표시하려면 글자 주위에 공백 없이 별표 두 개를 추가


### Italic
<u>asterisks(*)를 한 개</u> 추가 (예시 : `*text*` = *text*)
단어 중간을 이탤릭체로 표시하려면 글자 주위에 공백 없이 별표 한 개를 추가


### Blockquotes
인용문을 만들려면 단락 앞에  `>` 를 추가

```
> Kwonyezy is the best developer in the world.
>
> Factos 👍👀
```

> Kwonyezy is the best developer in the world.
>
> Factos 👍👀

# Lists
순서가 있는 목록과 순서가 없는 목록으로 구성 가능

### 순서가 있는 리스트
숫자와 마침표가 있는 항목을 추가

```
1. First item
2. Second item
3. Third item
4. Fourth item
```

1. First item
2. Second item
3. Third item
4. Fourth item

### 순서가 없는 리스트
각 항목 앞에 대시(`-`), 별표(`*`) 또는 더하기 기호(`+`)를 추가
하나 이상의 항목을 들여쓰면 중첩된 목록 생성 가능

```
* First item
- Second item
+ Third item
  * Fourth item
```

* First item
- Second item
+ Third item
  * Fourth item

# Code
단어나 구문을 코드로 표시하려면 backticks (`) 사용

|Markdown|HTML|Rendered Output|
|---|---|---|
|명령 프롬포트에 \`nano\`  입력|명령 프롬프트에 \<code>nano\</code> 로 입력|명령 프롬프트에 `nano` 로 입력|

### Escaping Backticks
하나 이상의 백틱(backtick)이 포함된 경우, 그 단어나 구절을 이중 백틱(``)으로 감싸서 이스케이프 가능

|Markdown|HTML|Rendered Output|
|---|---|---|
|\`\`마크다운 파일에 \`code\` 추가\`\`|\<code>마크다운 파일에 \`code\` 추가\</code>|``마크다운 파일에 `code` 추가``|

### Code Blocks
여러 줄의 코드에 걸쳐 있는 코드 블록을 만들려면 세 개 이상의 역따옴표( ``` ) 또는 물결( ~~ ) 안에 텍스트를 입력

```xml
<html>
  <head>
  </head>
</html>
```

```python
def foo():
  a = 1
  for i in [1,2,3]:
    a += i
```

# 수평선
한 줄에 3개 이상의 별표 (`***`), 대 (`---`), or 밑줄 (`___`) 을 입력

```text
***
---
_________________
```

# 링크
링크 텍스트를 괄호로 묶은 다음 (예시 : [League of Legends]) 바로 뒤에 괄호 안에 URL을 입력 (예시 : (https://www.leagueoflegends.com/ko-kr/))

```text
요즘 내가 즐겨하는 게임 [League of Legends](https://www.leagueoflegends.com/ko-kr/)
```

요즘 내가 즐겨하는 게임 [League of Legends](https://www.leagueoflegends.com/ko-kr/)


### 제목 추가

선택적으로 링크 제목 추가 가능
사용자가 링크 위로 마우스를 가져가면 도구 설명으로 표시
제목을 추가하려면 URL 뒤에 따옴표를 추가

```text
요즘 내가 즐겨하는 게임 [League of Legends](https://www.leagueoflegends.com/ko-kr/ "리그오브레전드")
```

요즘 내가 즐겨하는 게임 [League of Legends](https://www.leagueoflegends.com/ko-kr/ "리그오브레전드")


### URL 및 이메일 주소
URL이나 이메일 주소를 링크로 빠르게 변환하려면 해당 주소를 꺾쇠 괄호로 묶기

```text
<https://www.youtube.com/>
<kwonyezy@naver.com>
```

<https://www.youtube.com/>
<kwonyezy@naver.com>

# 이미지
느낌표 (`!`) 를 추가한 다음 괄호 (`[]`) 안에 대체 텍스트를 추가하고, 괄호 (`()`) 안에 이미지에 대한 경로 또는 URL을 추가

```text
![Tropical Paradise](/assets/img/example.jpg "Maldives, in October")
```

![Tropical Paradise](/assets/img/example.jpg "Maldives, in October")

### 이미지에 링크 추가
해당 이미지의 마크다운을 괄호로 묶은 다음 링크를 괄호 안에 추가

```text
[![La Mancha](/assets/img/La-Mancha.jpg "La Mancha: Spain, Don Quixote")](https://www.britannica.com/place/La-Mancha)
```

The rendered output looks like this: [![La Mancha](/assets/img/La-Mancha.jpg "La Mancha: Spain, Don Quixote")](https://www.britannica.com/place/La-Mancha)


# Escaping Characters
프로그래밍이나 마크업 언어에서 특정 문자를 특별한 의미로 인식하지 않도록 처리하는 방법
Markdown 문서에서 텍스트 서식을 지정하는 데 사용되는 리터럴 문자를 표시하려면 문자 앞에 백슬래시 (`\`) 추가

```text
\* Without the backslash, this would be a bullet in an unordered list.
```

\* Without the backslash, this would be a bullet in an unordered list.


### Escape 가능한 문자

|Character|Name|
|---|---|
|\`|backtick|
|\*|asterisk|
|\_|underscore|
|\{\}|curly braces|
|\[\]|brackets|
|\<\>|angle brackets|
|\(\)|parentheses|
|\#|pound sign|
|\+|plus sign|
|\-|minus sign \(hyphen\)|
|\.|dot|
|\!|exclamation mark|
|\||pipe|

# HTML
마크다운 형식의 텍스트에 HTML 태그를 사용이 가능하며, 특정 HTML 태그를 마크다운 문법 대신 사용하고 싶을 때 유용
텍스트의 색상을 지정하거나 이미지의 너비를 변경하는 등 요소의 속성을 변경해야 할 때도 HTML을 사용하는 것이 유용

```
이 단어는 **BOLD** 로 표현하였으며, 이 단어는 <span style="font-style: italic;">italic</span> 으로 표현.
```

이 단어는 **BOLD** 로 표현하였으며, 이 단어는 <span style="font-style: italic;">italic</span> 으로 표현.
