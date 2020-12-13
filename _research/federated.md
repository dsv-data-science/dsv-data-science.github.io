---
title: Federated learning
topic: explain

description: |


people:
  - Magnusson

layout: area
image: 
last-updated: 2020-11-07
---

<br>

## Description

Federated learning is an sub-area of machine learning that focuses on providing distributed and scalable algorithms for  training models across multiple decentralized peers without the need for sharing or exchanging data or information.

{% capture count_pub %}{% bibliography_count -q @*[keywords=optimization]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=optimization]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>
 
