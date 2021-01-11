---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---


<div class="content-wrap">
      <ol class="post-list">
        {% for post in site.posts %}
        <li>
          <h2 class="post-list__title"><a href="{{ post.url }}" title="访问 {{ post.title }}">{{ post.title }}</a></h2>
          <p class="post-list__excerpt">{{ post.content | strip_html | strip_newlines | truncate: 250 }}&hellip;</p>
          <div class="post-list__meta">
            <time datetime="{{post.date | date: date_to_xmlschema}}" class="post-list__meta--date date">{{ post.date | date: "%F"}}</time> 
            &#8226;<span class="post-list__meta--tags tags">{{ post.categories | join:' ' }}</span>
            &#8226; <span class="post-list__meta--tags tags">{{ post.tags | join:' ' }}</span>
            <a class="btn-border-small" href="{{ post.url }}">继续阅读</a>
           </div>
          <hr class="post-list__divider" />
        </li>
        {% endfor %}
      </ol>
</div>


