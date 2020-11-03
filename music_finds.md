---
layout: default
title: Radio Shows
---
<p class="message">
    Music, finds we ripped and uploaded to youtube for archival purposes.
</p>
<div class="posts">
  {% for post in site.categories.music_finds %}
  <article class="post">
    <h1 class="post-title">
      <a href="{{ post.url | relative_url }}">
        {{ post.artist}} - {{post.title}} ({{post.year}}, {{post.country}})
      </a>
    </h1>
    <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date">{{ post.date | date_to_string }}</time>
    
    <div class="vid-container">
        <iframe src="//www.youtube.com/embed/{{post.youtube_id}}" 
        frameborder="0" allowfullscreen class="video"></iframe>
    </div>
    {{ post.content }}
  </article>
  <hr>
  {% endfor %}
  
</div>

