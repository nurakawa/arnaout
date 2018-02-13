---
title: " "
layout: members_layout
permalink: /members-2.html
#sidebar:
#  nav: "members"
---

<h1 style="font-size:180%;"> The Arnaout Lab </h1>
<hr>
<br>

<!--Principal Invesigator-->

<h1 id="Principal-Investigator">Principal Investigator</h1>
<br>

{% for person in site.data.pi %}

<div class="row">
  <div class="column left">
    <img class="img-responsive" src="static/img/members/{{person.image}}">
    <br>
    <strong>{{person.name}}</strong>

    {% if person.position %} , {{person.position}} {% endif %}
    <br>
    <strong>Email</strong>: <em>{{person.email}}</em> 
    <br>
    {% if person.github %}
    <strong>Github</strong>: <a href= "https://github.com/{{person.github}}">{{person.github}} </a> <br>
    {% endif %}
    
    {% if person.website %}
    <strong>Web</strong>: <a href= "{{person.website}}">{{person.website}}</a> <br>
    {% endif %}
    
    {% if person.linkedin %}
    <strong>LinkedIn</strong>: <a href="http://linkedin.com/in/{person.linkedin}}">{{person.linkedin}}</a> <br>
    {% endif %}

    {% if person.scholar %}
    <a href= "http://scholar.google.com/citations?user={{person.scholar}}"> Scholar Citations </a> <br>
    {% endif %}
    
    {% if person.twitter %}
    <strong>Twitter</strong>: <a href= "http://twitter.com/{{person.twitter}}"> @{{person.twitter}} </a> <br>
    {% endif %}

  </div>

  <div class="column left">

    <p class="text-justify">{{person.description | markdownify}}</p>

  </div>
</div>
<hr>
{% endfor %}
<br>

<!--Members-->


<h1 id="Members">Members</h1>
<br>

{% for person in site.data.members %}

<div class="row">
  <div class="column left">
    {% if person.image %}
    <img class="img-responsive" src="static/img/members/{{person.image}}">
    <br>
    {% endif %}
    <strong>{{person.name}}</strong>

    {% if person.position %} , {{person.position}} {% endif %}
    <br>
    <strong>Email</strong>: <em>{{person.email}}</em> 
    <br>
    {% if person.github %}
    <strong>Github</strong>: <a href= "https://github.com/{{person.github}}">{{person.github}} </a> <br>
    {% endif %}
    
    {% if person.website %}
    <strong>Web</strong>: <a href= "{{person.website}}">{{person.website}}</a> <br>
    {% endif %}
    
    {% if person.linkedin %}
    <strong>LinkedIn</strong>: <a href="http://linkedin.com/in/{person.linkedin}}">{{person.linkedin}}</a> <br>
    {% endif %}

    {% if person.scholar %}
    <a href= "http://scholar.google.com/citations?user={{person.scholar}}"> Scholar Citations </a> <br>
    {% endif %}
    
    {% if person.twitter %}
    <strong>Twitter</strong>: <a href= "http://twitter.com/{{person.twitter}}"> @{{person.twitter}} </a> <br>
    {% endif %}

  </div>

  <div class="column left">

    <p class="text-justify">{{person.description | markdownify}}</p>

  </div>
</div>
<hr>
{% endfor %}
<br>


<!--Collaborators-->


<h1 id="Collaborators">Collaborators</h1>
<br>

{% for person in site.data.collaborators %}

<div class="row">
  <div class="column left">
    {% if person.image %}
    <img class="img-responsive" src="static/img/members/{{person.image}}">
    <br>
    {% endif %}
    <strong>{{person.name}}</strong>

    {% if person.position %} , {{person.position}} {% endif %}
    <br>
    {% if person.email %}
    <strong>Email</strong>: <em>{{person.email}}</em> 
    <br>
    {% endif %}
    {% if person.github %}
    <strong>Github</strong>: <a href= "https://github.com/{{person.github}}">{{person.github}} </a> <br>
    {% endif %}
    
    {% if person.website %}
    <strong>Web</strong>: <a href= "{{person.website}}">{{person.website}}</a> <br>
    {% endif %}
    
    {% if person.linkedin %}
    <strong>LinkedIn</strong>: <a href="http://linkedin.com/in/{person.linkedin}}">{{person.linkedin}}</a> <br>
    {% endif %}

    {% if person.scholar %}
    <a href= "http://scholar.google.com/citations?user={{person.scholar}}"> Scholar Citations </a> <br>
    {% endif %}
    
    {% if person.twitter %}
    <strong>Twitter</strong>: <a href= "http://twitter.com/{{person.twitter}}"> @{{person.twitter}} </a> <br>
    {% endif %}

  </div>

  <div class="column left">

    <p class="text-justify">{{person.description | markdownify}}</p>

  </div>
</div>
<hr>
{% endfor %}
<br>


<!--Alumni-->


<h1 id="Alumni">Alumni</h1>
<br>

{% for person in site.data.alumni %}

<div class="row">
  <div class="column left">
    {% if person.image %}
    <img class="img-responsive" src="static/img/members/{{person.image}}">
    <br>
    {% endif %}
    <strong>{{person.name}}</strong>

    {% if person.position %} , {{person.position}} {% endif %}
    <br>
    {% if person.email %}
    <strong>Email</strong>: <em>{{person.email}}</em> 
    <br>
    {% endif %}
    {% if person.github %}
    <strong>Github</strong>: <a href= "https://github.com/{{person.github}}">{{person.github}} </a> <br>
    {% endif %}
    
    {% if person.website %}
    <strong>Web</strong>: <a href= "{{person.website}}">{{person.website}}</a> <br>
    {% endif %}
    
    {% if person.linkedin %}
    <strong>LinkedIn</strong>: <a href="http://linkedin.com/in/{person.linkedin}}">{{person.linkedin}}</a> <br>
    {% endif %}

    {% if person.scholar %}
    <a href= "http://scholar.google.com/citations?user={{person.scholar}}"> Scholar Citations </a> <br>
    {% endif %}
    
    {% if person.twitter %}
    <strong>Twitter</strong>: <a href= "http://twitter.com/{{person.twitter}}"> @{{person.twitter}} </a> <br>
    {% endif %}

  </div>

  <div class="column left">
    {% if person.description %}
    <p class="text-justify">{{person.description | markdownify}}</p>
    {% endif %}

  </div>
</div>
<hr>
{% endfor %}



