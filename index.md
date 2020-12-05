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
        The <b>Data Science Research Group</b> at the <a href="https://dsv.su.se/en/research/research-areas/datascience/description">Department of Computer and Systems Sciences (DSV) of Stockholm University</a> focuses on core data science resarch as well as on application areas where data science can assist in providing useful insights towards decision making. The group focuses on the formulation of <strong>novel data science problems</strong> and the development of <strong>algorithmic methods</strong> and <strong>methodological pipelines</strong> for achieving scalable solutions in core application areas within <strong>social sciences</strong> and <strong>humanities</strong>.
    </p>
</div>

<div id="mainframe">
    <div class="maincol">
    <h2>Research</h2>    
   <p> The core research profile of the group is within machine learning and data mining, with emphasis on 
   <ul>
   <li>sequential and temporal data mining</li>
   <li>interpretable and explainable machine learning</li>
   <li>natural language processing</li>
   <li>reinforcement learning</li>
   <li>distributed optimization</li>
   <li>probabilistic modeling</li>
   </ul>
   </p>
<p>  The main application areas of the group include:
   <ul>
   <li>healthcare and wellbeing</li>
   <li>integrated vehicle health management and predictive maintanance</li>
   <li>public health policies for epidemics</li>
   <li>virtual reality and immersive technologies</li>
   <li>environmental sustainabiity</li>
   </ul>
   </p>
   <p>  A selection of our ongoing projects can be found below. For a list of all ongoing and completed projects of our group you can refer to our projects page. 
   </p>
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
