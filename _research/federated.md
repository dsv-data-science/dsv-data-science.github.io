---
title: Federated learning
topic: rl_fl

description: |


people:
  - Magnússon
  - Beikmohammadi
  - Vaishnav
  - Mondrejevski

layout: area
image: /img/areas/Federated.jpg
last-updated: 2022-09-01
---

<br>

## Description

Federated learning is an sub-area of machine learning that focuses on providing distributed and scalable algorithms for  training models across multiple decentralized peers without the need for sharing or exchanging data or information.

{% capture count_pub %}{% bibliography_count -q @*[keywords=federated]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=federated]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>
 
