---
layout: page
title : Tags
---
# Tags
<div class="tags-expo">
    <div class="tags-expo-list">
    {% assign sorted_tags = site.tags | sort %}
    {% for tag in sorted_tags %}
    <a href="#{{tag[0]}}" class="post-tag"><i class="fa-solid fa-tag" style="color: #004221;"></i> {{tag[0]|upcase}}</a>
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for tag in sorted_tags %}

    <h2 id="{{ tag[0] }}">{{tag[0]|upcase}}</h2>
    <ul class="tags-expo-posts">
      {% for post in tag[1] %}
        <a class="post-title" href="{{ post.url | relative_url }}">
      <li>
        {{ post.title }}
      <small class="post-date">{{ post.date | date_to_string }}</small>
      </li>
      </a>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>