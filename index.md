---
layout: page
title: "Home"
class: home
---

# Расcкажу Вам о себе ;) 

<div class="columns" markdown="1">

<div class="intro" markdown="1">
Я, IT Project Manager с наклонностями* :) Product Manager. Имею практическим опытом создания IT продуктов и управления IT проектами в IT/Fintech. По образованию [Инженер-механик](http://sazt-snu.in.ua/DesktopDefault.aspx). Закончил [Восточноукраинский национальный университет имени В. И. Даля ВНУ им. Даля](https://snu.edu.ua). В 2015 году прошел курс [Практика запуска стартапа](https://www.sikorskychallenge.com/startup-contest/) в стартап школе [Sikorsky Challenge](https://www.sikorskychallenge.com/стартап-школа/). Старт карьеры 2010 год от должности финансового менеджера отделения [Приват Банк] до IT диреткора финансовой компании [Экспресс Финанс]. В 2018 году основал компанию [Finceh](https://finceh.com). Компания, которой мы успешно управляем и помогаем партнерам запускать Fintech проекты.

Согласитесь! Нет ничего увлекательнее стартапов. И не спорьте ;) Ведь это путь от нуля до ста или от нуля к нулю. Удачи, не удачи, победа, старт, запуск.
Огромное удовольствие получаю от работы с командами разработки [Python](https://ru.wikipedia.org/wiki/Python) / [Django Framework](https://ru.wikipedia.org/wiki/Django) / [Blockcahin](https://ru.wikipedia.org/wiki/Блокчейн). Имею практический опыт создания Full Stack команд. От дизайна до сопровождения проектов.

Старатапы в моей жизни появились в 2014 году , погружен в финансовые технологии [Fintech](https://ru.wikipedia.org/wiki/Финансовые_технологии) работал над проектом [Sofast Money](https://www.youtube.com/watch?v=Y4bffq1vOjA), мой первый стартап, ставший финалистом конкурса [Sikorsky Challenge](https://www.sikorskychallenge.com). Согласитесь маленькое достижение, но именно с этого все началось.  Если вам интересен Fintech и стартапы - нам с вами по пути! 
Профессиотнальное упралвение IT инфраструктурой финансовых компаний и Pay Day Loan проектов.
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/dominik_berlin.webp' type='image/webp' />
  <img
    src='/images/dominik_berlin.jpg'
    alt='Dominik Moritz'/>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
* [Paul G. Allen Center](http://www.washington.edu/maps/?q=cse) Room [486](https://norfolk.cs.washington.edu/directory/index.php?prev_floor=4&show_room=CSE486)
</div>

</div>

В 2015 команда Sofast Money получила сервера от [Microsoft Bizspark ](https://en.wikipedia.org/wiki/Fulbright_Program). Что позовлило развить продукт и инфраструктуру. В конце 2015, в связи с отстуствем инвестиций и поголовным падением банков  было принято решение завершить проект. После чего команда перешла в разработку проектов на Blockchain. Детали карьеры в моем [CV]({{ "/cv/" | relative_url }}).

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
