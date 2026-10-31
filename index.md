---
layout: default
title: Home
---
<section class="hero">
  <h1>안녕하세요, 홍길동입니다.</h1>
  <p class="lead">[분야/관심사를 한 줄로] 예: 머신러닝 기반 신호처리를 연구하는 학생입니다.</p>
  <p>
    <a class="btn" href="{{ '/assets/cv.pdf' | relative_url }}">CV 다운로드 (PDF)</a>
    <a class="btn ghost" href="{{ '/cv/' | relative_url }}">이력 보기</a>
  </p>
</section>

<section>
  <h2>About</h2>
  <p>자기소개 3~5문장. 어떤 문제에 관심이 있고, 지금까지 무엇을 해왔고, 앞으로 무엇을 하고 싶은지 적습니다.</p>
  <ul>
    <li>Email: <a href="mailto:you@example.com">you@example.com</a></li>
    <li>GitHub: <a href="https://github.com/your-id">github.com/your-id</a></li>
    <li>LinkedIn: <a href="https://linkedin.com/in/your-id">linkedin.com/in/your-id</a></li>
  </ul>
</section>

<section>
  <h2>최근 글</h2>
  <ul class="post-list">
    {% for post in site.posts limit: 5 %}
    {% assign cat = site.data.categories | where: "key", post.category | first %}
    <li>
      <time>{{ post.date | date: "%Y.%m.%d" }}</time>
      <span>{% if cat %}<span class="chip">{{ cat.label }}</span>{% endif %}<a href="{{ post.url | relative_url }}">{{ post.title }}</a></span>
    </li>
    {% endfor %}
  </ul>
  <p><a href="{{ '/blog/' | relative_url }}">전체 글 보기 →</a></p>
</section>
