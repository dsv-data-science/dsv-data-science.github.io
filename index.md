---
layout: default
title: Home
notitle: true

# groups of columns of {roles: list, width: num, image: bool}
role-tables:
- - roles: [faculty]
    width: 6
    image: true
  - roles: [phd]
    width: 6
    image: true
- - roles: [researcher, collab]
    width: 6
    image: false
  - roles: [alumni, ugrad]
    width: 6
    image: false

---

<div class="jumbotron">
    <p>
        The <b>Data Science Research Group</b> is part of the <i>Department of Computer and Systems Sciences at Stockholm University</i>, more information found in <a href="https://dsv.su.se/en/research/research-areas/datascience/description"><b>this link</b></a>. The group focuses on:
        <ul>
            <li><strong>core data science research: </strong>including the development of methods, techniques and tools within the areas of machine learning, sequential and temporal data mining, interpretable and explainable machine learning, ensemble learning, and natural language processing.</li>
            <li><strong>core data science application areas:</strong> including learning from electronic health records, integrated vehicle health management, network traffic prediction, clinical text mining, and virtual reality.</li>
        </ul>
    </p>
</div>
    
<section>
    <h2>Research</h2>
    <div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.status != "inactive" %}
                {% include project-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>
</section>


<section>
    <h2>News</h2>
    <ul class="news list-unstyled">
        {% for post in site.posts limit: site.front_page_news %}
            {% include news-item.html item=post %}
        {% endfor %}
    </ul>
    {% assign numposts = site.posts | size %}
    {% if numposts >= 1 %}
        <p>
            <span class="fa fa-fw fa-history"></span>
            <a href="{{ site.base }}/blog.html">Older posts&hellip;</a>
        </p>
    {% endif %}
</section>


<div id="people">
    <h2>People</h2>
    {% for role-table in page.role-tables %}
        <section class="people row justify-content-between">
            {% for role-column in role-table %}
                <div class="col-md-{{ role-column.width }}">
                    {% for role in role-column.roles %}
                        {% include role-people.html role=role image=role-column.image %}
                    {% endfor %}
                </div>
            {% endfor %}
        </section>
    {% endfor %}
</div>
