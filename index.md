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
  - roles: [alumni]
    width: 6
    image: false

---

<div class="jumbotron">
<p>
        The <b>Data Science Research Group</b> at the <a href="https://dsv.su.se/en/research/research-areas/datascience/description">Department of Computer and Systems Sciences (DSV) of Stockholm University</a> focuses on core data science resarch as well as on application areas where data science can assist in providing useful insights for decision making. The group focuses on the formulation of <strong>novel data science problems</strong> and the development of <strong>algorithmic methods</strong> and <strong>methodological pipelines</strong> for achieving scalable solutions in core application areas within <strong>social sciences</strong> and <strong>humanities</strong>.
        </p>
</div>
<div id="mainframe">
    <div class="maincol">

<h2>Research</h2>    
<p>The core research profile of the group is within machine learning and data mining with emphasis on <b>sequential and temporal data mining</b>,  <b>explainable machine learning</b>,  <b>natural language processing</b>,  <b>reinforcement learning</b>, and  <b>distributed optimization</b>. Our focus application areas include  <b>healthcare and wellbeing</b>, <b>integrated vehicle health management and predictive maintanance</b>, <b>public health policies for epidemics</b>, <b>virtual reality and immersive technologies</b>, and <b>environmental sustainabiity</b>. </p>

<p>  A selection of our ongoing resaerch can be found below. For a comprehensive list of our research topics and profile please visit our <a href="research.html">research profile page</a>.</p>
   
   <div class="card-columns">
           {% comment %}
           Sort the projects by date, putting those without dates last
           {% endcomment %}
           {% assign research_by_date = site.research | sort: 'last-updated', 'first' %}
           {% assign research_by_date = research_by_date | reverse %}
           {% for r in research_by_date %}
               {% if r.highlight == "priority" %}
                   {% include researcharea-card.html project=r %}
               {% endif %}
           {% endfor %}
    </div>
    
<h2>Projects</h2>  
    <p>  A selection of our ongoing projects can be found below. For a comprehensive list of our projects please visit our <a href="projects.html">projects page</a>.
    </p>
   
<div class="card-columns">
        {% comment %}
        Sort the projects by date, putting those without dates last
        {% endcomment %}
        {% assign projects_by_date = site.projects | sort: 'last-updated', 'first' %}
        {% assign projects_by_date = projects_by_date | reverse %}
        {% for p in projects_by_date %}
            {% if p.highlight == "priority" %}
                {% include project-card.html project=p %}
            {% endif %}
        {% endfor %}
    </div>
    
   </div>
   
  <div class="rightcol">
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
    </div>
</div>

{% comment %}
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
{% endcomment %}
