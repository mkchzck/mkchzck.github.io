#---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

#layout: home
#---

---
title: "My Cayman Blog"
layout: default
---

# ようこそ！
Jekyll で作ったブログです。

<h1>最新の記事</h1>
<ul>
  {% for post in paginator.posts %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>

<div class="pagination">
  {% if paginator.previous_page %}
    <a href="{{ paginator.previous_page_path }}">前のページ</a>
  {% endif %}

  {% if paginator.next_page %}
    <a href="{{ paginator.next_page_path }}">次のページ</a>
  {% endif %}
</div>