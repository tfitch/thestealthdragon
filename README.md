## Welcome to The Stealth Dragon blog

Resurrected from the dead.

{% assign postsByYear =
    site.posts | group_by_exp:"post", "post.date | date: '%Y'" %}
{% for year in postsByYear %}
  <h1>{{ year.name }}</h1>
  <ul>
    {% for post in year.items %}
      <li>{{ post.date | date: "%B %-d, %Y" }}: <a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}
