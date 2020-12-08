---
layout: default
title: Research Profile
---
<br>
<div class="jumbotron">
<p>The core research profile of the group is within machine learning and data mining with emphasis on <b>sequential and temporal data mining</b>,  <b>explainable machine learning</b>,  <b>natural language processing</b>,  <b>reinforcement learning</b>, and  <b>distributed optimization</b>. Our focus application areas include  <b>healthcare and wellbeing</b>, <b>integrated vehicle health management and predictive maintanance</b>, <b>public health policies for epidemics</b>, <b>virtual reality and immersive technologies</b>, and <b>environmental sustainabiity</b>. </p>
</div>    
<div class="card-columns">
    {% comment %}
    Sort the projects by date, putting those without dates last
    {% endcomment %}
    {% assign projects_by_date = site.research | sort: 'last-updated', 'first' %}
    {% assign projects_by_date = projects_by_date | reverse %}
    {% for p in projects_by_date %}
        {% include researcharea-card.html project=p %}
    {% endfor %}
</div>

