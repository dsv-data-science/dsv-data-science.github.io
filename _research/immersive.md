---
title:  Time series analysis for behavioral modeling
topic: applications

description: |

people:
  - Quintero
  - Papapetrou
  - Hollmén

layout: area
image: /img/areas/immersive/loop-vr.png
last-updated: 2023-11-06
---

<br>

## Description

This research area focuses on the design, application and evaluation of machine learning methods to create behavioral models of users in digital environments. 

Our emphasis is the analysis of physiological time-series, motion trajectories, and game-play interactions within virtual reality (VR) and mixed reality (MR) systems, aiming to build models that perform real-time clustering and classification of subjective treats like user skill level, emotional states, or mental workload. We focus on XR technologies as a visualization mediums that provide 3D interactive immersive experience with prospective applications on healthcare (physical and mental rehab), professional training, education, or marketing. 

- How do immersive technologies enable new pathways for understanding the context in which a user interacts with a system?
- Can the user's behavioral and physiological data improve the accuracy of ML models estimating human factors?
- What are the challenges and risks of designing personalized systems that transcend current setups with a 2D-based display, touchscreen, keyboard, and mouse?

![immersive]({{ site.base }}/img/areas/immersive/loop-vr.png)

## Frameworks

- Luis Quintero's PhD thesis in the topic is [available online in this link](https://urn.kb.se/resolve?urn=urn:nbn:se:su:diva-222210)

- [Excite-O-Meter](https://github.com/luiqtr/exciteometer){:target="_blank"} - Easy Integration of behavioral time-series in digital environments. See [paper here](https://doi.org/10.1109/ISMAR52148.2021.00052)

![general]({{ site.base }}/img/areas/immersive/eom.png){:width="50%"}

- [Kinematic](https://github.com/luisqtr/kinemats){:target="_blank"} - Python library to analyze and classify head movement trajectories. See [paper here](https://doi.org/10.1109/AIVR52153.2021.00015)

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

## Projects

- [WALLENBERG]({{ site.base }}/projects/wallenberg.html)
- [EXTREMUM]({{ site.base }}/projects/extremum.html)

<br>
