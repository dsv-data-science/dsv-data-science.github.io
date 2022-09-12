---
title: TROPICAL
status: inactive

description: |
  Network traffic control and prediction using artificial intelligence  <br>
  <b>HW Flagship: 2019</b>

people:
  - Papapetrou

layout: project
image: "/img/projects/tropical/netw-traf-pred.png"
last-updated: 2019-06-19
---

## TROPICAL
**Project leader**:
- Panagiotis Papapetrou, Professor

**Researchers**
- Amin Azari, Postdoctoral Researcher

**Project period:** 2019-01-01 to 2019-09-31

**Funding:** Huawei (Flagship)

**Budget:** 100K USD

<br>

### Description
This project is a pilot study on the applicability of temporal machine learning methods, such as time series prediction and LSTM recurrent neural networks for network traffic identification and estimation. Moreover, it will evaluate the performance of random forests for temporal data series corresponding to network traffic for the task of network traffic identification. Finally, these techniques will then be incorporated to dynamically configure the DRX parameters in a simplified network model, hence providing substantial trade-offs between power reduction and network latency.

The main implementation steps include:
 * Time series prediction
 * Dynamic configuration of DRX

<div>
<img src="/img/projects/tropical/netw-traf-pred.png" width="70%" height="70%" />
</div>
<br>

### Implementation

- [network traffic dataset](https://github.com/AminAzari/cellular-traffic-analysis) - a data sample of our project used for network traffic prediction.


{% capture count_pub %}{% bibliography_count -q @*[keywords=temporal]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Results

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[project=networks]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}

