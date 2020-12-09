---
title: Distributed optimization and reinforcement learning

description: |


people:
  - Magnusson

layout: area
image: 
last-updated: 2020-11-07
---

<br>

## Description

---

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
 
## Implementations



<br>

## Related Projects

- [Project 1](../_projects/x.md)
