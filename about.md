---
layout: page
title: About
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

Atualmente faço parte da equipe de desenvolvimento na RoyalTI, também como conhecida como Estoque Sistemas, uma empresa de Paulo Afonso - BA focada atualmente ma distribuição e suporte em sistemas de automação comercial, mas que atualmente está investindo em novas soluções principalmente com Ruby on Rails, Angular e tecnologias emergentes.
