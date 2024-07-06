---
layout: page
title: "Home"
class: home
---

<div class="columns" markdown="1">

<div class="me" markdown="1">
<picture>
  <source srcset='/images/lynnegao.jpg' type='image/jpeg' />
  <img
    src='/images/lynnegao.jpg'
    alt='Lin Gao'>
</picture>


{:.no-list}
* <a href="mailto:{{ site.email }}"><i class="fas fa-envelope"></i>  {{ site.email }}</a>
* <a href="https://github.com/lynnegaogao"><i class="fab fa-github" aria-hidden="true"></i> lynnegaogao</a>
<a href="https://scholar.google.com/citations?user=9VqrBe0AAAAJ"><i class="fas fa-fw fa-graduation-cap" aria-hidden="true"></i> Lin Gao</a>
<!--<a href="https://scholar.google.com/citations?user=9VqrBe0AAAAJ"><i class="fas fa-id-card" aria-hidden="true"></i></a>-->
<!--<a href="https://twitter.com/Lynnegaogao"><i class="fab fa-twitter" aria-hidden="true"></i>Lynnegaogao</a>--> 
</div>

<div class="intro" markdown="1">
Hello, I'm Lin Gao (Lynne, 高琳), a master candidate at the School of Data Science, [Fudan University (FDU)](https://www.fudan.edu.cn/en/). I'm a member of the [FDUVIS Lab](https://fduvis.net/), where I work under the supervision of Prof. [Siming Chen](http://simingchen.me/). In 2023, I graduated from [Chongqing University (CQU)](https://english.cqu.edu.cn/) with a bachelor's degree in Data Science and Big Data Technology. At CQU, I was advised by Prof. [Haibo Hu](http://www.cse.cqu.edu.cn/info/2030/2497.htm) and was part of the [CQU-VIVA Lab](http://www.cquviva.cn/).
<br><br>
My research interests lie in Visual Analytics and Human-Computer Interaction. Specifically, I aim to advance *intelligent education* through visualization and interaction techniques. I'm exploring research related to human-AI collaboration with large language models.
<br><br>
<span class="bounce">🙋🏻‍♀️ I am actively seeking for PhD position of 25Fall!</span>

</div>

</div>


## <a href="{{ "/projects/" | relative_url }}">Projects</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>

<!--<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>-->

## <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<!--<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>-->

