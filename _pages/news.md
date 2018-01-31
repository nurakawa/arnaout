---
layout: splash
title: "News from the Arnaout Lab"
permalink: /news/
---


<h1> News from the Arnaout Lab </h1>
<hr>

<div class="w3-sidebar w3-bar-block" style="width:35%; float:left;">
<a class="twitter-timeline" data-lang="en" data-width="450" href="https://twitter.com/arnaoutlab?ref_src=twsrc%5Etfw">Tweets by arnaoutlab</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
</div>

<div style="margin-left:38%;">
<ul style="list-style: none;">
  {% for post in site.posts %}
    <li>
     <a href="{{ post.url }}">{{ post.title }}</a>
     {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

</div>
