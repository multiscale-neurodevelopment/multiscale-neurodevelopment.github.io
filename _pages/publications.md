---
title: "Publications"
layout: gridlay
excerpt: "Publications."
sitemap: false
permalink: /publications/
---


# Publications

### Recent news
- [L'Oreal For Women in Science Award](https://www.loreal.com/de-de/germany/pages/commitments/fwis/preistraegerinnen/)
- [Ones To Watch: Young Neuroscientists on the Rise](https://www.nature.com/articles/d41586-024-03049-2)
- [From Application to Award: How a Neuroscientist Secured the Emmy Noether Grant](https://gsonet.org/karrierewissen/casey-paquola-emmy-noether-grant/?lang=en)

### Group highlights

For more publications from the group, go to [Google Scholar](https://scholar.google.ch/citations?user=mKnsJ9AAAAAJ&hl=en)

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p><em>{{ publi.authors }}</em></p>
  <p><strong><a href="{{ publi.link.url }}">{{ publi.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>
