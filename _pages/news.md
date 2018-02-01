---
layout: splash
title: "News from the Arnaout Lab"
permalink: /news/
---
<style>
@media (min-width: 769px) {
    #news_content{
    margin-left:40%;
    }
}
    
@media (max-width: 768px) {
    #twitter_sidebar {
        display: none;
    }
    #news_content{
        margin-left: 0%;
    }
}
</style>

<h1> News from the Arnaout Lab </h1>
<hr>

<div id="twitter_sidebar" class="w3-sidebar w3-bar-block" style="width:35%; float:left;">
<a class="twitter-timeline" data-lang="en" data-dnt="true" href="https://twitter.com/arnaoutlab?ref_src=twsrc%5Etfw">Tweets by arnaoutlab</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
</div>


<div id="news_content">
<ul style="list-style: none;">
  {% for p in site.posts %}
    <li>
     <a href="{{ site.baseurl }}{{ p.url }}">{{ p.title }}</a>
     {{ p.excerpt }}
    </li>
  {% endfor %}
</ul>
