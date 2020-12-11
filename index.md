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

<!-- <div class="bannerarea">
    <div class="gridtile">
    <p> DataScienceGroup@DSV</p>
    </div>

</div> -->

<!-- <div class="jumbotron">
<p>
        
        </p>
</div> -->
<div id="mainframe" class="container">

<div id="welcome">
<h2>Welcome!</h2> 

    <p>
    The <b>Data Science Research Group</b> at the <a href="https://dsv.su.se/en/research/research-areas/datascience/description">Department of Computer and Systems Sciences (DSV) of Stockholm University</a> focuses on core data science resarch as well as on application areas where data science can assist in providing useful insights for decision making. The group focuses on the formulation of <strong>novel data science problems</strong> and the development of <strong>algorithmic methods</strong> and <strong>methodological pipelines</strong> for achieving scalable solutions in core application areas within <strong>social sciences</strong> and <strong>humanities</strong>.
    </p>

</div>

<div id="newscol">
    <div id="newswin">
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
    <div id="collaborators">
    <h2>Collaborators</h2>
    <p>H&M</p>
    <p>Scania</p>
    <p>Coop</p>
    <p>Spotify</p>
    <p>Folkhälsomyndigheten (Swedish Health Agency)</p>
    <p>SPV (Swedish Pension Agency)</p>
    <p>Arbetsförmedlingen (Swedish Unemployment Office)</p>
    </div>
</div>


<div id="maincol">
<h2>Research Profile</h2>    
<p>  A selection of our ongoing resaerch can be found below. For a comprehensive list of our research topics and research profiles please visit our <a href="research.html">research profile page</a>.</p>
   <!-- 1) Temporal Data Mining 2) Explainable ML 3) Applications -->
   <div class="researchwrapper" > 
      <div class="researchbox">Temporal Data Mining</div>
      <div style="flex: 1;">One of our focus areas is searching and mining rich and complex data sources, with emphasis on sequential and temporal data, histogram data, text, and graphs. In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs </div>
   </div>
   <div class="researchwrapper flexcrv" > 
   <div style="flex: 1;">One of our focus areas is searching and mining rich and complex data sources, with emphasis on sequential and temporal data, histogram data, text, and graphs. In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs </div>
   <div id="research2" class="researchbox">Explanable Machine Learning</div>
   </div>
   
   <div class="researchwrapper" > 
   <div id="research3" class="researchbox">Applications</div>
   <div style="flex: 1;">One of our focus areas is searching and mining rich and complex data sources, with emphasis on sequential and temporal data, histogram data, text, and graphs. In particular, we are interested in (1) learning predictive models, such as ensemble models, for classification of complex temporal data sources, such as univariate and multivariate time series, event sequences, sequences of temporal intervals, and graphs </div>
    
   </div>
   </div>






{% comment %}
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
    <p>  Our group is involved in several national and international projects. A selection of our ongoing projects can be found below. For a comprehensive list of our projects please visit our <a href="projects.html">projects page</a>.
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
{% endcomment %}



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
