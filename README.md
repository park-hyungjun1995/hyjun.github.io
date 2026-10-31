# 포트폴리오 + 블로그 (Jekyll / GitHub Pages)

## 글 쓰는 법
1. `_posts/` 폴더에 `YYYY-MM-DD-제목.md` 파일을 만든다 (제목은 영문/숫자/하이픈 권장).
2. 맨 위에 아래 형식을 적고, 그 아래에 Markdown으로 쓴다.

```
---
title: "글 제목"
category: paper-review   # paper-review | study | research-log
tags: [태그1, 태그2]
---
```

3. GitHub에 올리면 1~2분 뒤 사이트에 반영된다.

## 고칠 곳
- 이름, 사이트 설명: `_config.yml`
- 소개: `index.md` / 이력: `cv.md`
- 카테고리 추가: `_data/categories.yml`
- CV PDF: `assets/cv.pdf`
- 디자인: `assets/css/style.css`

수식은 `$...$`(인라인), `$$...$$`(별도 줄)로 쓴다.
날짜가 미래인 글은 그 날짜가 되기 전까지 표시되지 않는다.
