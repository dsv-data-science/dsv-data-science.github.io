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

...

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
 
## Implementations

- 

<br>

## Related Projects


