---
layout: default
title: "文件索引"
---

<h1>📄 文件索引页</h1>
<p>这里是所有报告的列表，由Jekyll自动生成。</p>

<ul>
  {% for report in site.reports %}
    <li>
      <a href="{{ report.url | relative_url }}">
        {{ report.title | default: report.name }}
      </a>
    </li>
  {% endfor %}
</ul>
