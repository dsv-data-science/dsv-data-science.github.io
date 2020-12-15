---
layout: default
title: Research Profile
---

<div class="container mt-3">

    <div class="jumbotron">
    <p>The core research profile of the group is within machine learning and data mining with emphasis on <b>sequential</b> and <b>temporal data mining</b>,  <b>explainable machine learning</b>,  <b>natural language processing</b>,  <b>reinforcement learning</b>, and  <b>distributed optimization</b>. Our focus application areas include  <b>healthcare</b>, <b>integrated vehicle health management</b>, <b>public health policies</b> for epidemics, <b>virtual reality</b> and <b>immersive technologies</b>, and <b>environmental sustainabiity</b>. </p>
    </div>
    <div class="profileanchor">    
    <h2 id="rprofile1"> Sequential and Temporal Mining </h2>
    </div>
    <a name="temporal"></a> 
    <div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.research | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.topic == "temporal" %}
                {% include researcharea-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>

    <div class="profileanchor">    
    <h2 id="rprofile2"> Explainable and Federated Learning</h2>
    </div>

    <a name="explain"></a> 
    <div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.research | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.topic == "explain" %}
                {% include researcharea-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>
    <div class="profileanchor">  
    <h2 id="rprofile3"> Machine Learning Applications </h2>
    </div>
    <a name="applixations"></a> 
    <div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.research | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.topic == "applications" %}
                {% include researcharea-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>


</div>
