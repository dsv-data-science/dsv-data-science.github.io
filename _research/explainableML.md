---
title: Model explainability and Fairness
highlight: priority
topic: explain

description: |

people:
  - Papapetrou
  - Lindgren
  - Samsten
  - Miliou
  - Kuratomi
  - Movin
  - Rugolon


layout: area
image: /img/areas/interpretable-models.png
last-updated: 2020-11-08
---

<br>

## Description

We focus on methods for generating interpretable and explainable models, such as counterfactual explanations, locally explainable models, and rule learning. Interpretability has gained more attention in recent years, since data science methods and models have started to be used to larger extend in both industry and society as a whole. It can be quantified at the model level, i.e., by providing a description of the whole model to the human or by instances, i.e., explaining for each decision the reasons and motivate behind the decision.  There exist lot of aspects on models that relate to interpretability, such as model stability and size, dimensionality reduction, and visualization. 

<img src="/img/projects/extremum/ABRANK.png">

{% capture count_pub %}{% bibliography_count -q @*[keywords=explainable]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=explainable]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}

<br>

## Implementations

- [wildboar](https://github.com/isaksamsten/wildboar) - explainable machine learning library for time series in Python

<br>

## Related Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)
- [AutoGrade]({{ site.base }}/projects/autograding.html)
- [3AI]({{ site.base }}/projects/3ai.html)
