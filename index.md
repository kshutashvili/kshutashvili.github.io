---
layout: page
title: "Home"
class: home
---

# Founder in Finceh LLC 

<div class="columns" markdown="1">

<div class="intro" markdown="1">
Founder/Product Owner в Finceh LLC более 10 лет опыта в IT из них 6 лет это Fintech. Образованию [Инженер-механик](http://sazt-snu.in.ua/DesktopDefault.aspx). Закончил [Восточноукраинский национальный университет имени В. И. Даля ВНУ им. Даля](https://snu.edu.ua). В 2015 году прошел курс [Практика запуска стартапа](https://www.sikorskychallenge.com/startup-contest/) . Курс "Project Manager 101" в PMClub. Курс "Basic Python" в SPALAH IT
Карьера: 
2010-2012. Финансовый менеджер отделения [Приват Банк] , 
2012-2013. Руководитель отделения группы В [Приват Банк], 
2015-2016. Главный специлист по облсуживанию интернет-проектов КЦ [Банк Михайловский], 2016-2017. Директор по развитию бизнеса [MACCALL], 2017-2019. IT диреткор финансовой компании [Экспресс Финанс]. 
Личные бизнес проекта проекты: [K2K](https://k2k.in.ua) - 2017, [TIME2PAY](https://time2pay.com.ua) - 2017, [Finceh](https://finceh.com) - 2018 , [TseCore](https://tsecore.finceh.com) - 2019, 
[FINK.AM](http://fink.am) - 2019

Практический опыт работы с командами разработки [Python](https://ru.wikipedia.org/wiki/Python) / [Django Framework](https://ru.wikipedia.org/wiki/Django) / [Blockcahin](https://ru.wikipedia.org/wiki/Блокчейн). Управление  Full Stack командами. 

Профессиональное управление IT инфраструктурой финансовых компаний и Pay Day Loan проектов.
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/dominik_berlin.webp' type='image/webp' />
  <img
    src='/images/dominik_berlin.jpg'
    alt='Aleksandr Kshutashvili'/>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* [Alex Kshutashvili](http://www.washington.edu/maps/?q=cse) Room [486](https://norfolk.cs.washington.edu/directory/index.php?prev_floor=4&show_room=CSE486)
</div>

</div>

Детали карьеры в моем [CV]({{ "/cv/" | relative_url }}).

## Последние проекты

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Больше проектов
</a>

## Последние публикации

<div class="featured-publications">
  {% for pub in site.data.publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{{ pub.venue }}, {{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Все публикации
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## News

<ul>
{% for news in site.data.news %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:14 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div>

</div>
