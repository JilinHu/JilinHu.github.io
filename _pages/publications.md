---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <div class="wordwrap">You can also find my articles on <a href="{{site.author.googlescholar}}">my Google Scholar profile</a>.</div>
{% endif %}

<ol class="pub-list">
{% for pub in site.publications reversed %}
  <li style="margin-bottom: 1.6em;">
    <strong>{{ pub.title }}</strong><br/>
    {{ pub.authors | replace: 'Jilin Hu', '<strong>Jilin Hu</strong>' }}<br/>
    <em>{{ pub.venue }}</em>, {{ pub.date | date: "%Y" }} &nbsp;&middot;&nbsp; <strong>{{ pub.ccf }}</strong>
    {%- if pub.authorship %} &nbsp;&middot;&nbsp; {{ pub.authorship }}{% endif %}
  </li>
{% endfor %}
</ol>
