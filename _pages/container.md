---
layout: splash
title: "home"
permalink: /container/
sidebar:
  nav: "members"
---

<div class="w3-sidebar w3-bar-block" style="width:35%; float:right;">
<h1> Alumni </h1>
{% for person in site.data.alumni %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:75%;">
    <div class="col-sm-4">
        {%if person.image %}
        <img class="img-responsive" src="static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:200px;height:200px"><br>
        {% endif %}
        <strong>{{person.name}}</strong><br>
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
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
{% endfor %}
</div>


<h1 id="Principal-Investigator">Principal Investigator</h1>
{% for person in site.data.pi %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:75%;">
    <div class="col-sm-4">
        <img class="img-responsive" src="../static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:200px;height:200px"><br>
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
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
{% endfor %}

<h1 id="Members">Members</h1>

<br>
{% for person in site.data.members %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:75%;">
    <div class="col-sm-4">
        {%if person.image %}
        <img class="img-responsive" src="../static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:200px;height:200px"><br>
        {% endif %}
        <strong>{{person.name}}</strong>, {{person.position}} <br>
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
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
{% endfor %}

<br>

<h1 id="Collaborators">Collaborators</h1>
<br>


{% for person in site.data.collaborators %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:75%;">
    <div class="col-sm-4">
        {% if person.image %}
        <img class="img-responsive" src="../static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:200px;height:200px"><br>
        {% endif %}
        <strong>{{person.name}}</strong>
        {% if person.position %} , {{person.position}} {% endif %}
        <br>
        {% if person.email %}
        <strong>Email</strong>: <em>{{person.email}}</em> 
        {% endif %}<br>
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
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
<hr>
{% endfor %}
