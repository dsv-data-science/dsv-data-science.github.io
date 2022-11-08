---
title:  Time series analysis for behavioral modeling
topic: applications

description: |

people:
  - Quintero
  - Papapetrou
  - Hollmén

layout: area
image: /img/areas/immersive/1generalArch.jpg
last-updated: 2022-01-22
---

<br>

## Description

This research area focuses on the design, application and evaluation of machine learning methods to create behavioral models of users in digital environments. Our emphasis is the analysis of physiological time-series, motion trajectories, and game-play interactions within virtual reality (VR) environments, aiming to build models that perform real-time clustering and classification of subjective treats like user skill level, emotional states, or mental workload. We focus on VR technology because it is a medium to enhance traditional tasks with interactive immersive experiences, and with many applications on healthcare (physical and mental rehab), professional training, education, or marketing. 

## Frameworks

- [Excite-O-Meter](https://github.com/luiseduve/exciteometer){:target="_blank"} - Easy Integration of behavioral time-series in digital environments. Check [paper](https://doi.org/10.1109/ISMAR52148.2021.00052)

![general]({{ site.base }}/img/areas/immersive/eom.png){:width="50%"}

- [Kinematic](https://github.com/luiseduve/kinemats){:target="_blank"} - Python library to analyze and classify head movement trajectories. See [paper](https://doi.org/10.1109/AIVR52153.2021.00015)

![general]({{ site.base }}/img/areas/immersive/head-mov.jpg){:width="50%"}

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
 
 <!-- THE PROJECT BELOW IS A COMMENT, IT IS NOT INCLUDED!! -->

{% comment %}
## Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)

{% endcomment %}
<br>
