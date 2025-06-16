---
layout: default
title: "歌曲索引"
---

<div class="container py-4">
  <header class="pb-3 mb-4 border-bottom">
    <h1 class="display-4">🎶 歌曲学习</h1>
  </header>

  <p class="lead">欢迎光临！这里汇集了一些歌曲的解析报告。</p>

  <ul class="list-group">
    {% for report in site.reports %}
      <li class="list-group-item d-flex justify-content-between align-items-center">
        <a href="{{ report.url | relative_url }}">
          {{ report.title | default: report.name }}
        </a>
        {% if report.author %}
          <span class="badge bg-primary rounded-pill">{{ report.author }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
