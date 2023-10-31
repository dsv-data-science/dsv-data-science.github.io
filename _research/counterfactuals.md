---
title: Counterfactual explanations
highlight: priority
topic: explain

description: |

people:
  - Papapetrou
  - Lindgren
  - Samsten
  - Miliou
  - Kuratomi
  - Wang

layout: area
image: /img/areas/counterfactual.png
last-updated: 2023-11-01
---

<br>

## Description

One of our main focus areas is methods for generating counterfactual explanations. Counterfactual explanations, a growing research area in artificial intelligence and machine learning, focus on generating hypothetical scenarios that reveal why a model made a particular decision. By exploring alternative inputs or model behaviors, we aim to enhance the transparency and interpretability of AI models, enabling users to better understand and trust their outcomes. This field holds promise for improving the accountability of AI applications across various domains, such as healthcare.


{% capture count_pub %}{% bibliography_count -q @*[keywords=explainable]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=counterfactual]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}

<br>

## Related Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)
- [AutoGrade]({{ site.base }}/projects/autograding.html)
- [3AI]({{ site.base }}/projects/3ai.html)
