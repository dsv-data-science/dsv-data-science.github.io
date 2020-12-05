---
layout: default
title: Ongoing Projects
---
<br>
<div class="jumbotron">
<p>
    Our group is involved in several national projects in the area of data science with applications to healthcare, law, public health policies for pandemics, and finance. Our current project collaborators include other academic/research institutions (e.g., KTH, RISE), public authorities (e.g., the Swedish Health Agency), healthcare providers (Karolinska Hospital, Karolinska Institute, Danderyds Hospital), as well as industrial peers. </p>
</div>    

<div class="card-columns">
    {% comment %}
    Sort the projects by date, putting those without dates last
    {% endcomment %}
    {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
    {% assign projects_by_date = projects_by_date | reverse %}
    {% for p in projects_by_date %}
        {% if p.status != "inactive" %}
            {% include project-card.html project=p %}
        {% endif %}
    {% endfor %}
</div>

<br>
# Completed Projects
<div class="jumbotron">
    The group has successfully completed several national and international projects in the broader area of data science and its applications. Our results comprise a number of peer-reviewed <a href="publications.html">publications</a>, source code packages, and demos.
</div> 

<div class="card-columns">
    {% comment %}
    Sort the projects by date, putting those without dates last
    {% endcomment %}
    {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
    {% assign projects_by_date = projects_by_date | reverse %}
    {% for p in projects_by_date %}
        {% if p.status == "inactive" %}
            {% include project-card.html project=p %}
        {% endif %}
    {% endfor %}
</div>

<br>

{% comment %}
# Project Details

|Acronym/Title|Funding Source| Period| Budget|
|---|---|---|:---:|
| **`IN PROGRESS`** |  |  |  |
| **EXTREMUM**: Explainable and Ethical Machine Learning for Knowledge Discovery from Medical Data Sources  | Digital Futures | 2020 - 2023 | 8.4M SEK |
| **3AI**: Automated Auditing using Artificial Intelligence, Swedish Research Council | Swedish Research Council | 2020 - 2022 | 3M SEK |
| **TEMPOMiner**: Temporal data mining for detecting adverse events in healthcare | Swedish Research Council | 2017 - 2020 | 3.4 MSEK |
| **`COMPLETED`** |  |  |  |
| **CODA**: Predictive models for interpretability and concept drift analytics | Vinnova/Scania | 2017 - 2020 | 18.2M SEK |
| **EXTREME**: Explainable and Ethical Machine Learning for Knowledge Discovery from Medical Data Sources | Digital Futures | 2019 - 2020 | 3.85M SEK |
| **CorIL**: Analyzing registry data to find ways to improve treatment of heart failure patients | Stockholm Region | 2017 - 2019 | 9M SEK |
| **TROPICAL**: Network traffic control and prediction using artificial intelligence | Huawei - Flagship | 2019 | 100K USD |
| **IRIS**: Forecasted individual maintenance support based on systematic knowledge of component states in inhomogeneous fleets of vehicles | Vinnova |  | 2012 - 2017 | - |
| **DADEL**: High-performance data mining for drug effect detection | SSF | 2012 - 2016 | 19M SEK |

{% endcomment %}
