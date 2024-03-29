---
layout: headerless_page
permalink: /research/
title: Research
---
# Publications

{% assign thumbnail="left" %}

{% for pub in site.data.publications %}
* {{pub.author}}.
[{{pub.title}}]({% if pub.internal %}{{pub.url | prepend: site.baseurl}}{% else %}{{pub.url}}{% endif %}).
*{{pub.journal}}*{% if pub.series %} ({{pub.series}}), {% endif %}{% if pub.pages %} pages {{pub.pages}}. {% endif %}{% if pub.publisher %} {{pub.publisher}}, {% endif %}{% if pub.location %} {{pub.location}}, {% endif %}{% if pub.month %} {{pub.month}} {% endif %}{% if pub.year %} {{pub.year}} {% endif %}  
{% if pub.doi %}[![DOI](../images/doi.svg "DOI")]({{pub.doi}}) {% endif %} {% if pub.media %}{% for item in pub.media %} [![{{item.name}}](../images/{{item.name | downcase }}.svg "{{item.name | replace:'RG','ResearchGate' | replace:'PDF','Preprint' }}")]({{item.url}}) {% endfor %}{% endif %}
{% endfor %}

# Academic Service

I am happy for a little academic service, during my PhD, as an additional reviewer for [ICPC 2017](https://www.computer.org/csdl/proceedings/icpc/2017/0535/00/0535z015.pdf), [SANER 2017](https://www.computer.org/csdl/proceedings/saner/2017/5501/00/07884601.pdf), [ICPC 2016](https://www.computer.org/csdl/proceedings/icpc/2016/1428/00/07503703.pdf), [ICSME 2015](https://www.computer.org/csdl/proceedings/icsme/2015/7532/00/07332445.pdf), and [ICSE 2015](https://www.computer.org/csdl/proceedings/icse/2015/1934/01/1934z037.pdf).
And also being part of the organization committee of [BENEVOL2017](http://ansymore.uantwerpen.be/events/BENEVOL2017) workshop. The proceedings of BENEVOL2017 [here](http://ceur-ws.org/Vol-2047/).

# Students
I have had the privilege to mentor (and learn from) following excellent students.

* [Gerardo Orellana](https://www.uantwerpen.be/en/education/international/international-students/international-degree-student/education-offer/testimonials/gerardo-orellana/) did his masters internship with us and worked on the [MSR 2017 mining challenge](http://2017.msrconf.org/#/challenge) to study the differences between unit and integration testing. His work eventually resulted in a [publication](../docs/MSR17_preprint.pdf) at MSR 2017.

* [Mathias Beke](https://denbeke.be) did his [masters thesis](https://denbeke.be/thesis/versions/mathias-beke-final.pdf) to compare the software quality attributes between client-side and server-side rendering technologies for the web development.

* [Wannes Ghielens](https://be.linkedin.com/in/wannesghielens) did his masters internship with us and evaluated the performance of different Android Layout Frameworks. His work is documented as a [technical report](../docs/ALF_technical_report_2018.pdf).

# PhD Thesis
* [Optimising and Assessing the Effectiveness of Spectrum Based Fault Localisation](../docs/PhD_thesis.pdf).
University of Antwerp, Belgium, 2018.

# MPhil Thesis
* [Policy-based Context-aware Architectural Adaptation in Pervasive Computing](../docs/MPhil_thesis.pdf).
University of Sindh, Jamshoro, 2014.
