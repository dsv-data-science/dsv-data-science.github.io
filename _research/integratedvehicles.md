---
title: Integrated vehicle management
topic: applications

description: |

people:
  - Lindgren
  - Kuratomi

layout: area
image: 
last-updated: 2020-11-04
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

- [CODA](../projects/coda.html)
- [IRIS](../projects/iris.html)
