---
layout: default
title: Research Profile
---

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
{% comment %}

*GitHub repository of the group <https://github.com/dsv-data-science>*

### Searching and mining sequential and temporal data

One of our focus areas is searching and mining rich and complex data sources, with emphasis on sequential and temporal data, histogram data, text, and graphs.  In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs, (2) building efficient indexing structures and searching techniques for complex data sources, (3) time series prediction and event burst detection using statistical methods and deep learning, and (4) subgroup and rule discovery in transactional and sequential data.

![sdm](/img/areas/sequential-temporal-data.png)


### Interpretable and explainable models

Another focus of our research within data science is on methods for generating interpretable and explainable models, e.g., actionable feature tweaking, locally explainable models, and rule learning. Interpretability has gained more attention in recent years, since data science methods and models have started to be used to larger extend in both industry and society as a whole. It can be quantified at the model level, i.e., by providing a description of the whole model to the human or by instances, i.e., explaining for each decision the reasons and motivate behind the decision.  There exist lot of aspects on models that relate to interpretability, such as model stability and size, dimensionality reduction, and visualization. 

![im](/img/areas/interpretable-models.png)

### Natural language processing

Particular focus is given on natural language processing with emphasis on efficient and resource lean methods for text summarization, classification, and word burst detection. Particular emphasis is given on clinical text mining by applying language technology, such as semantic analysis, to extract accurate and relevant information from very large clinical text sets. The latter is performed in close collaboration with the clinical text mining group.

### Learning from Electronic Health Records

The key aim is to develop and employ machine learning methods for providing efficient and effective decision support for healthcare and pharmaceutical research. The research group is currently focusing on two concrete problems: (1) learning temporal models for predicting and preventing adverse events in healthcare, such as Adverse Drug Events (ADEs) and (2) understanding heart failure and modeling heart failure patient treatment trajectories.  For the purposes of these two projects, our group has established strong collaboration with Stockholm County Council, Karolinska University Hospital, and Karolinska Institute.

![ehr](/img/areas/elec-hea-rec.jpg)

### Integrated vehicle management

The aim is to facilitate integrated vehicle health monitoring (IVHM) of heavy trucks. The focus then was to investigate how to predict the vehicle's health status by calculating the components remaining life to be able for create better decisions for example: (1) using health status to schedule maintenance so that unplanned downtime is minimized, (2) creating a system that optimizes maintenance plans based in part on the health status and customer preferences, and (3) creating a system that provides decision support to drivers and fleet planners utilization of vehicles. This project is implemented in strong collaboration with SCANIA.

### Immersive technologies and virtual reality

......

![ntp](....)

{% endcomment %}

