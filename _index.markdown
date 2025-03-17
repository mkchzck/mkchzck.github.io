---
layout: default
title: "ホーム"
---

<h2>最新の記事</h2>

<ul>
    {% for post in paginator.posts %}
        <li>
            <a href="{{ post.url | relative_url }}">{{ post.title }}</a> - {{ post.date | date: "%Y年 %m月 %d日" }}
        </li>
    {% endfor %}
</ul>

<!-- ページネーション -->
<div class="pagination">
    {% if paginator.previous_page %}
        <a href="{{ paginator.previous_page_path | relative_url }}">&laquo; 前のページ</a>
    {% endif %}
    <span>ページ {{ paginator.page }} / {{ paginator.total_pages }}</span>
    {% if paginator.next_page %}
        <a href="{{ paginator.next_page_path | relative_url }}">次のページ &raquo;</a>
    {% endif %}
</div>