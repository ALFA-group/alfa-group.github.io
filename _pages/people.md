---
title: "ALFA Lab - People"
layout: gridlay
excerpt: "ALFA Lab: Members"
sitemap: false
permalink: /people
---

## ALFA Staff
<div class="row">
{% include member_profile.html staff_data=site.data.people.alfa_staff type="alfa_staff"%}
</div>


## Graduate Students
<div class="row">
{% include member_profile.html staff_data=site.data.people.grad_students type="grad_students"%}
</div>


## Undergraduates
<div class="row">
{% include member_profile.html staff_data=site.data.people.undergrads type="undergrads"%}
</div>

## Active Collaborators
<div class="row">
{% include member_profile.html staff_data=site.data.people.collaborators type="collaborators"%}
</div>

## Past Visitors and Collaborators

{::nomarkdown}
<div class="full_collapse">
    <details>
      <summary>Full List</summary>
      <ul style="overflow: hidden">
      {% for member in site.data.people.past_visit_colab reversed%}
        {{ member.name }} <br>
      {% endfor %}
      </ul>
    </details>
</div>
{:/nomarkdown}

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
