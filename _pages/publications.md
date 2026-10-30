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
<li style="margin: 0 0 0.9em 0; line-height: 1.9;">
{%- if pub.doi %}<a href="https://doi.org/{{ pub.doi }}"><strong>{{ pub.title }}</strong></a>
{%- elsif pub.exturl %}<a href="{{ pub.exturl }}"><strong>{{ pub.title }}</strong></a>
{%- else %}<strong>{{ pub.title }}</strong>
{%- endif %}
<br/>
{{ pub.authors | replace: 'Jilin Hu', '<strong>Jilin Hu</strong>' }}
<br/>
<em>{{ pub.venue }}</em>{% if pub.pubinfo %}, {{ pub.pubinfo }}{% endif %}, {{ pub.date | date: "%Y" }}. <strong>{{ pub.ccf }}</strong>
</li>
{% endfor %}
</ol>
