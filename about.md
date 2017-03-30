---
layout: page
title: About me
---

{% comment %}
  This inserts the "about" photo and text from `_config.yml`.
  You can edit it there (jekyll needs restart!) or remove it and provide your own photo/text.
  Don't forget to add the `me` class to the photo, like this: `![alt](src){:.me}`.
{% endcomment %}

{% if site.author.photo %}
  ![{{ site.author.name }}]({{ site.author.photo }}){:.me}
{% endif %}

{{ site.author.about }}

Sou ex-acadêmico em Sistemas de Informação pela Faculdade 7 de Setembro (Paulo Afonso-BA).

Desde agosto de 2016 faço parte da equipe de desenvolvimento do Instituto Padre Pio, empresa situada em Cuiabá e Londrina.

Para ver outros trabalhos meus, acesse: [Linkedin](https://www.linkedin.com/in/anchieta-j%C3%BAnior-69568630/).

Hoje minhas atividades estão focadas em Ruby on Rails e Javascript, além de Front-End quando necessário.

Também sou GDG Lead e Organizer em Paulo Afonso, do qual tenho bastante orgulho em fazer parte e contribuir.
