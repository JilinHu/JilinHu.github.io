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
<li style="margin: 0 0 0.75em 0;">
<strong>{{ pub.title }}</strong><br/>
{{ pub.authors | replace: 'Jilin Hu', '<strong>Jilin Hu</strong>' }}.
<em>{{ pub.venue }}</em>{% if pub.pubinfo %}, {{ pub.pubinfo }}{% endif %}, {{ pub.date | date: "%Y" }}.
<strong>{{ pub.ccf }}</strong>{% if pub.authorship %} ({{ pub.authorship }}){% endif %}
{%- if pub.doi %} &middot; <a href="https://doi.org/{{ pub.doi }}">DOI</a>{% endif %}
{%- if pub.exturl %} &middot; <a href="{{ pub.exturl }}">Paper</a>{% endif %}
</li>
{% endfor %}
</ol>
