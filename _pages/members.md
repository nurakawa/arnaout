---
title: The Arnaout Lab
layout: archive
permalink: /members/
---

{% for person in site.data.members %}
<hr>
<!-- The paddingtop and margin-top edits allow anchors to link properly. -->

<div id = "{{person.name}}" class="row" style="padding-top: 60px; margin-top: -60px;">
    <div class="col-sm-4">
        <img class="img-responsive" src="{{person.image}}" style="align:left;border-radius:50%;width:200px;height:200px"><br>
        <strong>{{person.name}}</strong>, {{person.position}} <br>
        <em>{{person.email}}</em> <br>
        {% if person.github %}
          <a href= "http://github.com/{{person.github}}"></a> <br>
        {% endif %}
        {% if person.website %}
          <a href= "{{person.website}}">{{person.website}}</a> <br>
        {% endif %}
        {% if person.orcid %}
          <a href="http://orcid.org"><img class="inline-block" src="/static/img/orcid_logo.png"></a>
          <a href="http://{{person.orcid}}"> {{person.orcid}}</a> <br>
        {% endif %}
        {% if person.scholar %}
          <a href= "http://scholar.google.com/citations?user={{person.scholar}}"> Scholar Citations </a> <br>
        {% endif %}
        {% if person.twitter %}
          <a href= "http://twitter.com/{{person.twitter}}"> @{{person.twitter}} </a> <br>
        {% endif %}
    </div>
    <div class="col-sm-8">
        <p class="text-justify">{{person.description | markdownify}}</p>
    </div>
</div>
{% endfor %}


