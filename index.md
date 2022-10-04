---
layout: default
title: Home
notitle: true

# # groups of columns of {roles: list, width: num, image: bool}
# role-tables:
# - - roles: [faculty, postdoc]
#     width: 6
#     image: true
#   - roles: [phd]
#     width: 6
#     image: true
# - - roles: [researcher, collab]
#     width: 6
#     image: false
#   - roles: [alumni]
#     width: 6
#     image: false
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
    The <b>Data Science Research Group</b> at the <a href="https://dsv.su.se/en/research/research-areas/datascience/description">Department of Computer and Systems Sciences (DSV) of Stockholm University</a> focuses on core data science resarch as well as on application areas where data science can assist in providing useful insights for decision making. The group focuses on the formulation of <strong>novel data science problems</strong> and the development of <strong>algorithmic methods</strong> and <strong>methodological workflows</strong> for achieving scalable solutions in core application areas within <strong>social sciences</strong> and <strong>humanities</strong>.
</p>


<div id="maincol">
<h2>Research Profile</h2>    
<p> The group has three main focus research themes: <b>sequential and temporal mining</b>, <b>explainable and federated</b> learning, and machine learning <b>applications</b>.  For a comprehensive list of our research topics please visit our <a href="research.html">research page</a>.</p>
   <!-- 1) Temporal Data Mining 2) Explainable ML 3) Applications -->
   <div class="researchwrapper" > 
      <div class="researchbox" onclick="location.href='research.html#rprofile1'">Sequential & Temporal Mining</div>
      <div style="flex: 1;">We focus on developing methods for searching and mining rich and complex data sources, with emphasis on sequential and temporal data, as well as text. In particular, we are interested in defining temporal abstractions and extracting high-utility features for clustering or classification of sequential and temporal data sources, such as univariate and multivariate time series, event sequences, and text. </div>
   </div>
   <div class="researchwrapper flexcrv" > 
   <div style="flex: 1;">We give particular emphasis on methods and workflows for explainable machine learning. We explore both model agnostic and model specific solutions, as well as counterfactual explanation formulations for sequential data variables, images, and text. Our main goal is to provide scalable and distributed solutions for maintaining good trade-offs between predictive performance and explainability.  Moreover, we are interested in solutions that can function in a distributed manner without the need for data exchange.
   </div>
   <div id="research2" class="researchbox" onclick="location.href='research.html#rprofile2'">Explainable & Federated Learning</div>
   </div>
   
   <div class="researchwrapper" > 
   <div id="research3" class="researchbox" onclick="location.href='research.html#rprofile4'">Machine Learning Applications</div>
   <div style="flex: 1;">Our methods and solutions are motivated by real-world applications and use cases. The group has particular expertise in mining and model understanding from healthcare and medical data sources. In addition, we have established a strong expertise in predictive maintenance and integrated vehicle management. Finally, we are interested in financial data, environmental data, as well as data emerging from immersive technologies, such as virtual reality.</div>
    
   </div>
</div>

</div>

<div id="newscol">
    <div id="newswin">
    <h2>News</h2>
    <ul class="news list-unstyled">
        {% for post in site.posts limit: 4 %}
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
    <p><img src="https://www.folkhalsomyndigheten.se/gui/i/logo.png?v=1.4.25.0" width ="100%"></p>
    <br>
    <p><img src="img/logo/AF-logga1.png" width="100%"  style="horizontal-align:middle"></p>
    <br>
    <p><img src="img/logo/HM-group.jpg" width ="100%" style="horizontal-align:middle"></p>
    <p><img src="https://www.coop.se/contentassets/a2726990fdc948efbb5fb5e917bb2dec/coop_topbild_700x260.png" width ="100%" style="horizontal-align:middle"></p>    
    <br>
    <p><img src="https://www.scania.com/content/dam/scanianoe/market/master/homepage/scania-wordmark.svg" width ="100%" style="horizontal-align:middle"></p>    
    <br>
    <p><img src="img/logo/sp_logo.png" width ="100%" style="horizontal-align:middle"></p>
    <br>
    <p>SPV (Swedish Pensions Agency)</p>
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
   
<!--   

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
{% endcomment %} -->
