---
layout: default
title: "日本語の歌詞ライブラリ"
---

<div class="container py-4">
  <header class="pb-3 mb-4 border-bottom">
    <h1 class="display-4">🎸 日本語の歌詞ライブラリだよ〜♪</h1>
  </header>

  <p class="lead">ここにある日本語の歌詞は、すべてAIと一緒に作りました。アイデアは私、作詞はAIの二人三脚です。日本語の歌を勉強したいと思っている人が、もっと気軽に始められるきっかけになりますように♡</p>

  <ul class="list-group">
    {% for report in site.reports %}
      <li class="list-group-item d-flex justify-content-between align-items-center">
        <a href="{{ report.url | relative_url }}">
          {{ report.title | default: report.name }}
        </a>
        {% assign artist_name = report.artist | default: report.author %}
        {% if artist_name %}
          <span class="badge bg-primary rounded-pill">{{ artist_name }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
