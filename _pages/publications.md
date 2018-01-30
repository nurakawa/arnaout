---
layout: splash
title: Publications
permalink: /publications/
---
<!--
<style>
img{
-webkit-filter: opacity(70%); /* Safari */
    filter: opacity(70%);
}
</style>
-->

<h1>Publications</h1>


<div class="container-fluid">
{% for publication in site.data.publications%}
<hr>
<div class="row" style="padding-top: 60px; margin-top: -60px;" id="{{publication.pmid}}">

<div style="font-size: 80% !important;">{{ publication.citation | markdownify }}</div>
	<div class="col-sm-6" style="font-size: 80%;">
		<img class = "img-responsive" src = "{{publication.image}}" style="max-height: 180px" hspace="20" align="left">
		<br>
	<ul class="col-sm-6">			
	        <!--PMID-->
			<li>PMID: <a href="http://www.ncbi.nlm.nih.gov/pubmed/{{publication.pmid}}" alt = "pubmed link: {{publication.pmid}}"> {{publication.pmid}}</a></li>
			
			<!--PMCID - optional -->
			{% if publication.pmcid %}
			<li>PMCID: <a href="http://www.ncbi.nlm.nih.gov/pmc/articles/{{publication.pmcid}}" alt = "pubmed central link: {{publication.pmcid}}"> {{publication.pmcid}}</a></li>
			{% endif %}
			
			<!--Biorxiv - optional -->
			{% if publication.biorxiv %}
			<li>Biorxiv Preprint: <a href="http://dx.doi.org/10.1101/{{publication.biorxiv}}" alt = "biorxiv prepring link: {{publication.pmcid}}"> {{publication.biorxiv}}</a></li>
			{% endif %}
			
			<!-- PDF -->
			{% if publication.pdf %}
			<li><a href="{{publication.pdf}}" alt = "PDF"> Full Text</a></li>
			{% endif %}
			
			<!-- Datasets - optional -->
			{% if publication.data %}
			<li>Online Dataset{% if publication.data.size > 1 %}s{% endif %}: 
				{% if publication.data.size > 1 %}
				<ul>
					{% for dataset in publication.data %}
					<li><a href="http://dx.doi.org/{{dataset}}" alt = "sbgrid data repository">doi:{{dataset}}</a></li>
					{% endfor %}
				</ul>
				{% else %}
				<a href="http://dx.doi.org/{{publication.data}}" alt = "sbgrid data repository">doi:{{publication.data}}</a>
				{% endif %}
			</li>
			{% endif %}
			
			<!--PDBS - optional-->
			{% if publication.pdbs %}
			<li>Deposited Structure{% if publication.pdbs.size > 1 %}s{% endif %}: 
				{% for code in publication.pdbs %}
				<a href="http://www.rcsb.org/pdb/explore/explore.do?structureId={{code}}">{{code}}</a>{% unless forloop.last %}, {% endunless %}
				{% endfor %}
			</li> 
			{% endif %}
			<!--Extra junk-->
			<!--<strong>Additional Links</strong>-->
			{% for link in publication.links %}
			<li><a href="{{link.url}}" alt="{{link.name}}">{{link.name}}</a></li>
			<br>
			{% endfor %}
	</ul>
	</div> 
</div> 
<br>
<br>
{% endfor %}
</div>

