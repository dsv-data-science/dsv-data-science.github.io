---
title:  Immersive technologies and virtual reality
topic: applications

description: |

people:
  - Quintero


layout: area
image:
last-updated: 2020-11-03
---

<br>

## Description
The main focus of this area is on how to exploit machine leaerning methods for improving user experience within the area of immersive technologies. Our emphasis is on applying time series clustering and early classification techniques for modeling user skills and capabilities when using virtual reality applications.

{% capture count_pub %}{% bibliography_count -q @*[keywords=immersive]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=immersive]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>
 
 {% comment %}
## Implementations

## Projects

{% endcomment %}
<br>
