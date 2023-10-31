---
title: Reinforcement learning
topic: rl_fl

description: |


people:
  - Magnússon
  - Dinis Jr
  - Piller
  - Beikmohammadi
  - Vaishnav

layout: area
image: /img/areas/RL.jpg
last-updated: 2022-09-02
---

<br>

## Description

Reinforcement Learning is the sub-field of AI that deals with how an software agent learns optimal decisions from data and by exploration.  Our focus is on algorithm development and theory for advancing reinforcement learning to healthcare and social science. In particular, we focus on:
1. Constrained exploration, e.g., in terms of fairness, safety
2. Reinforcement learning from logged data and off-policy methods 
3. Economic and resource efficient reinforcement learning. 

{% capture count_pub %}{% bibliography_count -q @*[keywords=reinforcement]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=reinforcement]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
{% comment %}
## Implementations

{% endcomment %}

<br>
## Related Projects

- [Covid-Sim]({{ site.base }}/projects/covid.html)