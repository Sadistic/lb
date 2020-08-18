<ul>
  {% for news in site.news %}
    <li>
      <a href="{{site.baseurl}}{{ news.url }}">{{ news.title }}</a>
    </li>
  {% endfor %}
</ul>