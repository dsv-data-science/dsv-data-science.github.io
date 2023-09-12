---
layout: default
title: People

# groups of columns of {roles: list, width: num, image: bool}
role-tables:
- - roles: [faculty, affiliated]
    width: 6
    image: true
  - roles: [phd]
    width: 6
    image: true
# - - # Empty left column
#   - roles: [researcher]
#     width: 6
#     image: true
- - roles: [collab]
    width: 6
    image: false
  - roles: [alumni]
    width: 6
    image: false
---

<div id="people" class="container mt-3">
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
