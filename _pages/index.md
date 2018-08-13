---
layout: defaults/page
permalink: index.html
narrow: true
---

{% include components/intro.md %}

### [More about Goktug]({{ site.baseurl}}{% link _pages/about.md %})

### Recent Posts

{% for post in site.posts limit:3 %}
{% include components/post-card.html %}
{% endfor %}


