---
layout: page
permalink: /publications/
title: Publications
---

{% assign thumbnail="left" %}

{% for pub in site.data.publications %}
* {{pub.author}}.
[{{pub.title}}]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}).
*{{pub.journal}}*{% if pub.series %} ({{pub.series}}), {% endif %}{% if pub.pages %} pages {{pub.pages}}. {% endif %}{% if pub.publisher %} {{pub.publisher}}, {% endif %}{% if pub.location %} {{pub.location}}, {% endif %}{% if pub.month %} {{pub.month}} {% endif %}{% if pub.year %} {{pub.year}} {% endif %}{% if pub.doi %}[[DOI]({{pub.doi}})]{% endif %}{% if pub.media %}{% for article in pub.media %}[[{{article.name}}]({{article.url}})]{% endfor %}{% endif %}
{% endfor %}

# MPhil Thesis
* [Policy-based Context-aware Architectural Adaptation in Pervasive Computing](../docs/MPhil_thesis.pdf).
University of Sindh, Jamshoro, 2014.