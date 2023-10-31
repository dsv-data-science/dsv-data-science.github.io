---
title: Mining complex sequential patterns
highlight: priority
topic: temporal
description: |

people:
  - Papapetrou
  - Samsten
  - Hollmén
  - Miliou
  - Lee
  - Wang
  - Rugolon
  - Kreuzer

layout: area
image: /img/areas/sequential-temporal-data.png
last-updated: 2020-11-11
---


## Description

One of our focus areas is mining rich and complex data sources, with emphasis on sequential and temporal data, histogram data, text, and graphs.  In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs, (2) time series prediction and event burst detection using statistical methods and deep learning, and (3) subgroup and rule discovery in transactional and sequential data.

{% capture count_pub %}{% bibliography_count -q @*[keywords=temporal]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=temporal]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>
 
## Implementations

- [wildboar](https://github.com/isaksamsten/wildboar) - explainable machine learning library for time series in Python

<br>

## Related Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)
- [TEMPOMiner]({{ site.base }}/projects/tempominer.html)
- [TROPICAL]({{ site.base }}/projects/TROPICAL.html)
