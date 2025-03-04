---
title: "ALFA Lab - Research"
layout: textlay
excerpt: "ALFA Lab -- Research"
sitemap: false
permalink: /research/
---

# Research Projects

<div class="col-sm-12">

{% assign grouped_projects_by_year = site.data.research.research_topics | sort: "start_year" | reverse %}
{% for project in grouped_projects_by_year %}
<!-- <div class="row" style="border: 1px solid #000; border-radius: 2% / 6%"> -->
<div class="row">

<div class="col-sm-4">
<img src="{{ site.url }}{{ site.baseurl }}/images/research/{{project.photo}}" class="img-responsive" width="100%" height="100%" style="float: left; margin-bottom: 0" />
{% if project.photo_source %}
<i style="margin: 0">Image Source: {{project.photo_source}}</i>
{% endif %}
</div>

<div class="col-sm-8 clearfix">

#### {{project.title}}

{{project.description}}

**Team Members:** <i>{{project.members}}</i>

{% if project.collaborators %}
**Collaborators:** <i>{{project.collaborators}}</i>
{% endif %}

</div>
</div>
<br>
{% endfor %}
</div>


