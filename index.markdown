---
layout: default
title: "歌曲索引"
---

<div>
  <!-- <header>
    <h1>🎶 歌曲学习</h1>
  </header> -->

  <!-- <p>欢迎光临！这里汇集了一些歌曲的解析报告。</p> -->

  <ul>
    {% for report in site.reports %}
      <li>
        <a href="{{ report.url | relative_url }}">
          {{ report.title | default: report.name }}
        </a>
        {% if report.author %}
          <span>{{ report.author }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</div>
