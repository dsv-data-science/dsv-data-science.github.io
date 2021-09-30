---
title:  Behavioral user modelling in virtual reality
topic: applications

description: |

people:
  - Quintero
  - Papapetrou
  - Hollmen

layout: area
image: /img/areas/immersive/1generalArch.jpg
last-updated: 2020-11-01
---

<br>

## Description

This research area focuses on the design, application and evaluation of machine learning methods to create behavioral models of users in digital environments. Our emphasis is the analysis of physiological time-series, motion trajectories, and game-play interactions within virtual reality (VR) environments, aiming to build models that perform real-time clustering and classification of subjective treats like user skill level, emotional states, or mental workload. We use VR as out testbed because it is a powerful medium to enhance traditional tasks with interactive immersive experiences, and with many applications on healthcare (physical and mental rehab), professional training, education, or marketing. 

<!-- The general **framework** comprises six building blocks and involves the use of **time-series analysis** and **reinforcement learning**:

![general]({{ site.base }}/img/areas/immersive/1generalArch.jpg){:width="70%"}  -->

## Frameworks

- [Excite-O-Meter](https://github.com/luiseduve/exciteometer){:target="_blank"} - Easy Integration of time-series analysis in Virtual Reality

![general]({{ site.base }}/img/areas/immersive/eom.png){:width="50%"}

- [PARE-VR](https://github.com/luiseduve/pare-vr){:target="_blank"} - Physiologically Adaptable Relaxation Experience through Virtual Reality

![general]({{ site.base }}/img/areas/immersive/2physioArchit.png){:width="50%"}

<br>

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
## Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)

{% endcomment %}
<br>
