
{% for category in site.data.links_categories %}
 <h2><a href="#{{ category.category | slugify }}">{{ category.category }}</a></h2>
 <p>
 {% for tag in category.tags %}
   [<a href="#{{ tag.tag }}">{{ tag.tag }}</a>]
 {% endfor %}
 </p>
{% endfor %}


{% for category in site.data.links_categories %}
 {{ "# " | append: category.category | markdownify }}
 {% for tag in category.tags %}
   <h3><a name="{{ tag.tag }}"> {{ tag.tag }} </a></h3>
   {% for link in site.data.links %}
   {% assign category_match = false %}
   {% assign tag_match = false %}
   {% if link.category == category.category %}
   {% assign category_match = true %}
   {% endif %}
   {% for linktag in link.tags %}
   {% if linktag == tag %}
   {% assign tag_match = true %}
   {% endif %}
   {% endfor %}
   {% if category_match and tag_match %}
   *  {{link.description}} [[Link]]({{link.link}})
     {% if link.document-url %}[[PDF]({{link.document-url}})]{% endif %}
     {% if link.date %} <p class="dateadded"> --- added on [{{link.date}}] </p> {% endif %}
   {% endif %}
   {% endfor %}
 {% endfor %}
{% endfor %}
