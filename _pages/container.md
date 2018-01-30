---
layout: splash
title: Container
permalink: /container/
toc: true
---
<h1>Publications</h1>
<hr>
<br>
<!--SOLUTION TO OVERFLOW PROBLEM: https://stackoverflow.com/questions/19695784/how-can-i-make-bootstrap-columns-all-the-same-height-->

<style>
.row{
    overflow: hidden; 
}

[class*="col-"]{
    margin-bottom: -99999px;
    padding-bottom: 99999px;
}
</style>


<div class="container-fluid">
{% for publication in site.data.publications%}

<div class="row justify-content-between" style="padding-top: 60px; margin-top: -60px;">
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-4">
  <!--<div class="my-img"><img src='http://via.placeholder.com/250x250' align="left" hspace="20"></div>-->
  
  <img class = "img-responsive" src = "{{publication.image}}" style="max-width: 250px" hspace="20" align="left">
  
  </div>
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-8-auto" style="font-size:75%">
  {{ publication.citation | markdownify }}
  <ul style="list-style-type:none">
    
    <!--PMID - mandatory-->
    <li> 
    <strong>PMID</strong>: <a href="http://www.ncbi.nlm.nih.gov/pubmed/{{publication.pmid}}" alt = "pubmed link: {{publication.pmid}}"> {{publication.pmid}}</a>  
    
    <!--PMCID - optional-->
    {% if publication.pmcid %}
	<strong>PMCID</strong>: <a href="http://www.ncbi.nlm.nih.gov/pmc/articles/{{publication.pmcid}}" alt = "pubmed central link: {{publication.pmcid}}"> {{publication.pmcid}}</a>
	{% endif %}
	</li>
    
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
  <br>
  </div>
</div> 
<hr>
{% endfor %}
</div>

