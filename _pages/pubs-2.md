---
layout: splash
title: Publications
permalink: /pubs-2/
---

<h1>Publications</h1>
<hr>
<br>
<!--SOLUTION TO OVERFLOW PROBLEM: https://stackoverflow.com/questions/19695784/how-can-i-make-bootstrap-columns-all-the-same-height-->

<style>
li{
    padding:0;
    /*margin-top: -2px;*/
}
.row{
    overflow: hidden; 
}

[class*="col-"]{
    margin-bottom: -99999px;
    padding-bottom: 99999px;
}
</style>


<div class="container-fluid">

<!--Sorting by date-->
{% assign sorted = (site.data.publications | sort: 'date') | reverse %}

{% for publication in sorted %}

<div class="row justify-content-between" style="padding-top: 60px; margin-top: -60px;">
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-4">
  
  <!--<img class = "img-responsive" src = "{{publication.image}}" style="max-width: 380px" hspace="20" align="left">-->
  <img class = "img-responsive" src = "{{publication.image}}" style="width: 420px" hspace="20" align="left">
  </div>
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-8-auto" style="font-size:105%">
  {{ publication.title | markdownify }}
 
  
  <ul style="font-size:70%; list-style-type:none;">
    <li>{{ publication.authors | markdownify }}</li>
    <li>{{ publication.journal}} {{publication.year}}</li>
    {% if publication.pmid %}
    <!--PMID - optional-->
    <li> 
    PMID: <a href="http://www.ncbi.nlm.nih.gov/pubmed/{{publication.pmid}}" alt = "pubmed link: {{publication.pmid}}"> {{publication.pmid}}</a> 
    
    <!--PMCID - optional-->
    {% if publication.pmcid %}
	PMCID: <a href="http://www.ncbi.nlm.nih.gov/pmc/articles/{{publication.pmcid}}" alt = "pubmed central link: {{publication.pmcid}}"> {{publication.pmcid}}</a>
	{% endif %}
	</li>
    {%endif%}
    <!--PDF - optional-->
    {% if publication.pdf %}
	<li><a href="{{publication.pdf}}" alt = "PDF"> Full Text</a></li>
	{% endif %}
    
    <!--URL - optional-->
    {% if publication.url %}
	<li><a href="{{publication.url}}" alt = "URL"> Full Text</a></li>
	{% endif %}
	
	<!--doi - optional
    {% if publication.doi %}
	<li><a href="http://{{publication.doi}}" alt = "doi"> doi </a></li>
	{% endif %}-->
    
  </ul>
  
  </div>
</div> 
<hr>
{% endfor %}
</div>

