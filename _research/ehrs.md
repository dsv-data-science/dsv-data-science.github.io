---
title: Learning from electronic health records
highlight: priority
topic: applications

description: | 

people:
  - Papapetrou
  - Asker
  - Bampa
  - Rebane

layout: area
image: /img/areas/elec-hea-rec.jpg
last-updated: 2022-01-24
---

<br>

## Description

The key aim is to develop and employ machine learning methods for providing efficient and effective decision support for healthcare and pharmaceutical research. The research group is currently focusing on two concrete problems:

1. Learning temporal models for predicting and preventing adverse events in healthcare, such as Adverse Drug Events (ADEs)
2. Understanding heart failure and modeling heart failure patient treatment trajectories. 

For the purposes of these two projects, our group has established strong collaboration with Stockholm County Council, Karolinska University Hospital, and Karolinska Institute.

{% capture count_pub %}{% bibliography_count -q @*[keywords=temporal]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=healthcare]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}

<br>

## Implementations

<br>

## Related Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)
- [COVID]({{ site.base }}/projects/covid.html)
