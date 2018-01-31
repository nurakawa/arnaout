---
layout: splash
title: "Contact"
permalink: /container/
---


<h1> Contact the Arnaout Lab </h1>
<hr>

<div class="w3-sidebar w3-bar-block" style="width:25%; float:right; background-color:lightgrey;">
<strong>Rima Arnaout</strong>, Assistant Professor <br>
  Division of Cardiology, Department of Medicine <br>
  University of California, San Francisco <br>
  email: rima.arnaout (#!) ucsf.edu <br> 
  555 Mission Bay Blvd South Rm 484 
  San Francisco, CA 94158
</div>

<div style="margin-right:26%;">
<ul style="list-style: none;">
  {% for post in site.posts %}
    <li>
     <a href="{{ post.url }}">{{ post.title }}</a>
     {{ post.excerpt }}
    </li>
  {% endfor %}
</ul>

</div>
