---
title: Natural language processing
topic: temporal

description: |

people:
  - Pavlopoulos
  - Randl

layout: area
image: /img/areas/nlp-example.png
last-updated: 2020-11-10
---

<br>

## Description

Particular focus is given on Natural Language Processing with emphasis on efficient and resource lean methods for language modeling (e.g., predictive keyboards), text generation and classification (e.g, from radiograph to diagnostic text), as well as information extraction (e.g., toxic spans detection). Particular emphasis is given on language technology applied on medical texts, to extract accurate and relevant information from very large clinical text sets. The latter is performed in close collaboration with the clinical text mining group.

{% capture count_pub %}{% bibliography_count -q @*[keywords=nlp]* %}{% endcapture %}
{% if count_pub != "0" %}
<br>

## Latest publications

<div class="publications">
    <table class="table">
        <tbody>
        <tr>
          {% bibliography -q @*[keywords=nlp]*  -- max 10 %}
        </tr>
        </tbody>
    </table>
</div>
{% endif %}
 
 <br>

## Related Projects

- [EFRA]({{ site.base }}/projects/efra.html)
- [EXTREMUM]({{ site.base }}/projects/extremum.html)
- [AutoGrade]({{ site.base }}/projects/autograding.html)
- [NLP-assisted troubleshooting]({{ site.base }}/projects/nlp_assisted_troubleshooting.html)
