---
title: "Team"
layout: gridlay
excerpt: "Team members"
sitemap: false
permalink: /team/
---

# Group Members

 **We are open to applications from interested PhD students, Postdocs, and Master students. Send an introductory email and your CV to casey.paquola@gmail.com**
 See the full advertisement [here](https://github.com/multiscale-neuroanatomy/multiscale-neuroanatomy.github.io/blob/master/Ausschreibung_PhD.pdf) and apply using this [form](https://www.fz-juelich.de/portal/EN/Careers/application/_node.html?cms_hre_link_id=oh1wsgAdJZQXLhy1&cms_lang=en)

{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }} <!--<br>email: <{{ member.email }}></i> -->
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}


# Collaborators

We work closely with the [MICA lab](https://mica-mni.github.io/) at the Montreal Neurological Institute (MNI), McGill University, Canada. 

