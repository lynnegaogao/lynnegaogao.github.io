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
* <a href="mailto:{{ site.email }}"><i class="fas fa-envelope"></i> Email: {{ site.email }}</a>
* <a href="https://github.com/lynnegaogao"><i class="fab fa-github" aria-hidden="true"></i> Github: lynnegaogao</a>
* <a href="https://scholar.google.com/citations?user=9VqrBe0AAAAJ"><i class="fas fa-fw fa-graduation-cap" aria-hidden="true"></i> Google Scholar: Lin Gao</a>
* <a href="https://twitter.com/Lynnegaogao"><i class="fab fa-twitter" aria-hidden="true"></i> Twitter: Lynnegaogao</a> 
</div>

<!--<div class="content" markdown="1">-->
<div class="intro" markdown="1">
Hello, I'm Lin Gao (Lynne, 高琳), a first-year graduate student at the School of Data Science, [Fudan University (FDU)](https://www.fudan.edu.cn/en/). I'm a member of the [FDUVIS Lab](https://fduvis.net/), where I work under the supervision of Prof. [Siming Chen](http://simingchen.me/). In 2023, I graduated from [Chongqing University (CQU)](https://english.cqu.edu.cn/) with a bachelor's degree in Data Science and Big Data Technology, where I was advised by Prof. [Haibo Hu](http://www.cse.cqu.edu.cn/info/2030/2497.htm) and was part of the [CQU-VIVA Lab](http://www.cquviva.cn/).
<br><br>
My research interests lie in Visual Analytics and Human-Computer Interaction. Specifically, I aim to advance *intelligent education* through visualization and interaction techniques. I'm exploring research related to human-AI collaboration with large language models.
<br><br>
📢 News    
<span class="bounce">🙋🏻‍♀️ I am actively seeking for PhD position of 25Fall!</span>
<div class="news" markdown="1">
<div class="news-content">
<ul>
  <li>
    <div class="news-item">
      <div class="news-content">
        - Arrive in Hong Kong and start my 3-months visit to HKUST VisLab.
      </div>
      <time class="news-date">2024-07-03</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
        - Our work <i>FinDecipher</i> is accepted by ChinaVis 2024.
      </div>
      <time class="news-date">2024-06-20</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
      - Attend VIS 2023 in Melbourne and present our work <i>TransforLearn</i>.
      </div>
      <time class="news-date">2023-10-26</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
      - Start my graduate study at the School of Big Data Science, FDU.
      </div>
      <time class="news-date">2023-09-01</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
      - Our work <i>TransforLearn</i> is accepted by VIS 2023.
      </div>
      <time class="news-date">2023-07-16</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
      Graduate from CQU with a bachelor's degree.
      </div>
      <time class="news-date">2023-06-28</time>
    </div>
  </li>
</ul>
</div>
</div>

</div>

<!--<div class="news" markdown="1">
## News

<ul>
  <li>
    <div class="news-item">
      <div class="news-content">
        Received the Best Paper Award at the XYZ Conference.
      </div>
      <time class="news-date">2024-07-01</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
        Presented at the ABC Workshop on Visual Analytics.
      </div>
      <time class="news-date">2024-06-15</time>
    </div>
  </li>
  <li>
    <div class="news-item">
      <div class="news-content">
        Started a new research project on intelligent education.
      </div>
      <time class="news-date">2024-05-20</time>
    </div>
  </li>
</ul>
</div>-->


<!--</div>-->


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

