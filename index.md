---
layout: default
title: Bienvenu chez Louis
whereami: index
---

#### Bienvenu chez Louis.Zhibin.Lv

### Profil
Je suis ingénieur en informatique. J'ai travaillé dans ce domaine pendant 10 ans en maîtrisant Python, Java, SQL, etc.

Maintenant, je suis en train d'étudier le programme de Maîtrise en informatique à l'Université de Montréeal au Canada, spécialiste l'Intelligence artificielle.

J'aime nager, jouer au badminton et voyager.


---

### Coordonnées:

* <i class="fa fa-envelope"></i> [louis.lv.info@gmail.com](mailto:louis.lv.info@gmail.com)
* <i class="fa fa-linkedin"></i> <http://louis-udm.github.io>


---

### Liste:

<div class="post-list-body">
    <div post-cate="All">
        <ul>
            {% for post in site.posts %}
            <li>{{ post.date | date:"%Y-%m-%d" }} <a href="{{ post.url }}"> {{ post.title }}</a></li>
            {% endfor %}
        </ul>
    </div>
    {% for tag in site.tags %}
      <div post-cate="{{tag | first}}">
        <ul>
        {% for posts in tag  %}
          {% for post in posts %}
            {% if post.url %}
              <li>{{ post.date | date:"%Y-%m-%d" }} <a href="{{ post.url }}"> {{ post.title }}</a></li>
            {% endif %}
          {% endfor %}
        {% endfor %}
        </ul>
      </div>
    {% endfor %}
</div>