---
title: " "
layout: splash
permalink: /members.html
#sidebar:
#  nav: "members"


---

<h1 id="Principal-Investigator">Principal Investigator</h1>
<br>
{% for person in site.data.pi %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:85%;">
    <div class="col-sm-4">
        <img class="img-responsive" src="static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:280px;height:280px">
	<br> <br>
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

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:85%;">
    <div class="col-sm-4">
        {%if person.image %}
        <img class="img-responsive" src="static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:280px;height:280px">
	<br><br>
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
<!--<hr style="height:4px; border:none; color:#000; background-color:#000; width:15%; text-align:left; margin: 5 5 0 5;">-->
{% endfor %}

<br>

<h1 id="Collaborators">Collaborators</h1>
<br>


{% for person in site.data.collaborators %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px; font-size:85%;">
    <div class="col-sm-4">
        {% if person.image %}
        <img class="img-responsive" src="static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:280px;height:280px">
	<br> <br>
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


<h1 id="Alumni">Alumni</h1>
<br>

{% for person in site.data.alumni %}

<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 0px; margin-top: -60px; font-size:85%;">
    <div class="col-sm-4">
        {% if person.image %}
        <img class="img-responsive" src="static/img/members/{{person.image}}" style="align:left;border-radius:50%;width:280px;height:280px">
	<br><br>
        {% endif %}
        <strong>{{person.name}}</strong>
        {% if person.position %} ,{{person.position}} {% endif %}
        <br>
        {% if person.email%}
        <strong>Email</strong>: <em>{{person.email}}</em> 
        <br>
        {%endif%}
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
