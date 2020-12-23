---
title:  Immersive technologies and virtual reality
topic: applications

description: |

people:
  - Quintero


layout: area
image: /img/areas/immersive/1generalArch.jpg
last-updated: 2020-11-01
---

<br>

## Description

The main focus of this area is on how to exploit machine learning methods for improving user experience within the area of immersive technologies. Our emphasis is on applying time series analysis and early classification techniques for modeling user skills and capabilities when using virtual reality (VR) applications.

VR is a powerful medium to enhance traditional learning tasks with interactive immersive experiences in areas like *education, physical rehabilitation, psychological therapies, professional training, or marketing*. We explore how **real-time data science** can enable the creation of training virtual tasks that can automatically adapt and personalize to a specific user based on estimation of skill level based on ML-based methodological workflows.

The general **framework** comprises six building blocks and involves the use of **time-series analysis** and **reinforcement learning**:

![general]({{ site.base }}/img/areas/immersive/1generalArch.jpg){:width="70%"}

## Implementations

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
