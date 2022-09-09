---
title: Integrated vehicle management
topic: applications

description: |

people:
  - Lindgren
  - Kuratomi

layout: area
image: /img/areas/vehicle_management.jpg
last-updated: 2022-01-23
---

<br>

## Description

The aim is to facilitate integrated vehicle health monitoring (IVHM) of heavy trucks. The focus then was to investigate how to predict the vehicle's health status by calculating the components remaining life to be able for create better decisions for example: (1) using health status to schedule maintenance so that unplanned downtime is minimized, (2) creating a system that optimizes maintenance plans based in part on the health status and customer preferences, and (3) creating a system that provides decision support to drivers and fleet planners utilization of vehicles.

{% capture count_pub %}{% bibliography_count -q @*[keywords=vehicles]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=vehicles]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>
 
 {% comment %}
## Implementations

{% endcomment %}

<br>

## Related Projects

- [RAPIDS]({{ site.base }}/projects/rapids.html)
- [NLP-assisted troubleshooting]({{ site.base }}/projects/nlp_assisted_troubleshooting.html)
- [CODA]({{ site.base }}/projects/coda.html)
- [IRIS]({{ site.base }}/projects/iris.html)
