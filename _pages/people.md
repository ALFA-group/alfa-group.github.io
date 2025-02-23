---
title: "ALFA Lab - People"
layout: gridlay
excerpt: "ALFA Lab: Members"
sitemap: false
permalink: /people
---

# Group Members
ALFA is dedicated to cultivating an inclusive culture that supports, promotes, and empowers diverse voices in Computer Science & AI

## ALFA Staff
<div class="row">
{% for member in site.data.people.alfa_staff %}
<div class="col-sm-6 clearfix">
  {% include staff_image.html photo=member.photo %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.role }}</i>
  {% if member.email %}
  Email: [{{member.email}}](mailto:{{member.email}})
  {% endif %}
  <ul style="overflow: hidden">
  {% for info in member.info %}
    <li>{{ info }}</li>
  {% endfor %}
  </ul>
</div>
{% assign index = forloop.index | modulo: 2 %}
{% if index == 0 and forloop.last == false %}
  </div><div class="row">
{% endif %}
{% endfor %}
</div>


## Graduate Students
<div class="row">
{% for member in site.data.people.grad_students %}
<div class="col-sm-6 clearfix">
  {% include staff_image.html photo=member.photo %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.role }}</i><br>
  Research Area(s):
  <ul style="overflow: hidden">
  {% for info in member.info %}
    <li>{{ info }}</li>
  {% endfor %}
  </ul>
</div>
{% assign index = forloop.index | modulo: 2 %}
{% if index == 0 and forloop.last == false %}
  </div><div class="row">
{% endif %}
{% endfor %}
</div>


## Undergraduates
<div class="row">
{% for member in site.data.people.undergrads %}
<div class="col-sm-6 clearfix">
  {% include staff_image.html photo=member.photo %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.role }}</i><br>
  <ul style="overflow: hidden">
  {% for info in member.info %}
    <li>{{ info }}</li>
  {% endfor %}
  </ul>
</div>
{% assign index = forloop.index | modulo: 2 %}
{% if index == 0 and forloop.last == false %}
  </div><div class="row">
{% endif %}
{% endfor %}
</div>

## Collaborators
<div class="row">
{% for member in site.data.people.collaborators %}
<div class="col-sm-6 clearfix">
  {% include staff_image.html photo=member.photo %}
  <h4>{{ member.name }}</h4>
  <i>{{ member.role }}</i><br>
  <ul style="overflow: hidden">
  {% for info in member.info %}
    <li>{{ info }}</li>
  {% endfor %}
  </ul>
</div>
{% assign index = forloop.index | modulo: 2 %}
{% if index == 0 and forloop.last == false %}
  </div><div class="row">
{% endif %}
{% endfor %}
</div>


## Alumni
<div class="row">

<div class="col-sm-3 clearfix">
<h4>Postdocs</h4>
{% for member in site.data.people.alumni_postdocs reversed%}
{{ member.name }} ({{member.end_year}})
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
<h4>PhD Students</h4>
{% for member in site.data.people.alumni_phds reversed%}
{{ member.name }} ({{member.end_year}})
{% endfor %}
</div>

<div class="col-sm-3 clearfix">
  <h4>Masters Students</h4>
  <ul style="overflow: hidden">
  {% assign grouped_students = site.data.people.alumni_masters | group_by: "end_year" | reverse %}
  {% for year_group in grouped_students %}
    <details>
      <summary>{{ year_group.name }}</summary>
      <ul style="overflow: hidden">
        {% for member in year_group.items %}
          {{ member.name }} ({{member.type}})<br>
        {% endfor %}
        </ul>
    </details>
  {% endfor %}
  </ul>
</div>

<div class="col-sm-3 clearfix">
  <h4>Undergraduate Students</h4>
  <ul style="overflow: hidden">
  {% assign grouped_students = site.data.people.alumni_undergrads | group_by: "end_year" | reverse %}
  {% for year_group in grouped_students %}
    <details>
      <summary>{{ year_group.name }}</summary>
      <ul style="overflow: hidden">
        {% for member in year_group.items %}
          {{ member.name }} ({{member.type}})<br>
        {% endfor %}
        </ul>
    </details>
  {% endfor %}
  </ul>
</div>
