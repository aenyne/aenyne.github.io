---
layout: page
title: The Very Hungry Datapillar
subtitle: A blog about Data and AI ethics
---
![image](https://user-images.githubusercontent.com/56920075/183063769-120e8a56-0b97-4260-b667-b7ce00a181ac.png)


In the light of the moon, a little app lay on a leaf. <br>
One Sunday morning, the warm sun came up and pop! – out of the app came a tiny and very hungry datapillar.  <br>
He started to look for some food.  <br>
On Monday he ate through one like. But he was still hungry.  <br>
On Tuesday, he ate through two reviews, but he was still hungry.  <br>
On Wednesday, he ate through three pictures, but he was still hungry.  <br>
On Thursday, he ate through four shopping carts, but he was still hungry.  <br>
On Friday, he ate through five social media profiles, but he was still hungry.  <br>
On Saturday he ate through views, movenment recording, network connections, friend's posts, health app reports, face marks, emotional replies, fitness trackers, credit reviews, doctor's accounts. That night he had a stomachache!  <br>
  <br>
Now, do you think it's Sunday again?
<br>
<br>
<div>
{% assign postsCategory = site.posts | group_by_exp:"post", "post.categories"  %}
{% for category in postsCategory %}
<h4 class="post-teaser__month">
<strong>
{% if category.name %} 
- - - - -  {{ category.name }} - - - - - 
{% else %} 
{{ Print }} 
{% endif %}
</strong>
</h4>
<ul class="list-posts">
{% for post in category.items %}
<li class="post-teaser">
<a href="{{ post.url | prepend: site.baseurl }}">
<span class="post-teaser__title">{{ post.title }}</span>
<span class="post-teaser__date">{{ post.date | date: "%d %B %Y" }}</span>
</a>
</li>
{% endfor %}
</ul>
{% endfor %}
</div>
