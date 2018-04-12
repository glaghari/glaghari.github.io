{% for news in site.data.news %}
 * [{{news.date}}] --- {{news.title}}
{% endfor %}
