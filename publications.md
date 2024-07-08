---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications



{% assign pubyears = site.publications | group_by:"year"  %}
{% assign sorted_pubyears = pubyears | reverse %}
{% for year in sorted_pubyears %}
  <div class="year-block">
  <hr class="year-divider" />
    {% assign sorted_pubs = year.items | sort: 'title' %}
    {% for pub in sorted_pubs %}
      {% include publication.html pub=pub %}
    {% endfor %}
    <div class="year-label">{{ year.name }}</div>
  </div>
{% endfor %}

<script>
  {% include itemsjs.min.js %}
  {% include pubfilter.js %}
</script>
