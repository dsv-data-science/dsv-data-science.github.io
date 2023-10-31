---
title: Nowcasting and Forecasting
highlight: priority
topic: temporal
description: |

people:
  - Papapetrou
  - Miliou
  - Kreuzer

layout: area
image: /img/areas/nowcasting-example.png
last-updated: 2020-11-09
---


## Description

One of our focus areas is nowcasting and forecasting, with emphasis on sequential and temporal data. Using Big Data deriving from everyday life as external proxies, it is possible to nowcast and forecast the evolution of phenomena whose study relies only on historical data or data that come with a significant lag. We work mainly on epidemics, healthcare, peace, and sentiment.
<!--In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs, (2) building efficient indexing structures and searching techniques for complex data sources, (3) time series prediction and event burst detection using statistical methods and deep learning. -->

{% capture count_pub %}{% bibliography_count -q @*[keywords=temporal]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=nowcasting]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}

<br>

## Related Projects

- [EXTREMUM]({{ site.base }}/projects/extremum.html)
