---
layout: default
title: Publications

years: [2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013,
       1956, 1950, 1935, 1905]
---
<p>
    <a href="{{ site.base }}/bib/papers.bib">Download BibTeX.</a>
</p>

<div class="publications">
    <table class="table">
        <tbody>
            {% for y in page.years %}
                <!-- Show only the years that have papers -->
                {% capture count_year %}{% bibliography_count -q @*[year={{y}}]* %}{% endcapture %}
                {% if count_year != "0" %}
                    <tr>
                        <td>
                            <!-- <span class="date"> -->
                                <h2 class="year">{{y}}</h2>
                            <!-- </span> -->
                        </td>
                        <td>
                            <span class="totalpubs">
                                <b> Total: {{count_year}} </b>
                            </span>
                        </td>
                    </tr>
                    <tr>
                        <td>
                        </td>
                        <!-- Each publication generates a row -->
                        {% bibliography -q @*[year={{y}}]* %}
                    </tr>
                {% endif %}
            {% endfor %}
        </tbody>
    </table>
</div>