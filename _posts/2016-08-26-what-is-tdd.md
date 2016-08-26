---
layout: post
title: O que é TDD? Serve pra quê?
tags: [hyde]
---

<style>
  .preview {
    display: none;
  }

  @media (min-width: 48em) {
    .preview {
      display: block;
    }
  }
</style>

## Introdução
TDD ou Test-Driven Development, que nosso querido PT-BR pode ser traduzido como Desenvolvimento Orientado a Testes é uma metodologia de desenvolvimento derivada do XP (Extreme Programming) que tem como principal função reduzir bugs e garantir uma melhor qualidade no código escrito, além de manter documentado um projeto, basicamente seguindo os seguintes passos:

* Pensar em algo que será desenvolvido.
* Escrever um teste para esta funcionalidade.
* Fazer com que o teste falhe (claro, nada foi implementado ainda além do teste).
* Programar a funcionalidade pensada.
* Executar o teste novamente e garantir que dessa vez o teste passe.
* "Refatorar" o código escrito e garantir que o mesmo esteja limpo, de fácil entendimento e principalmente correto em relação as convenções de Orientação à Objetos.

Seguindo esses conceitos, podemos entender o ciclo do TDD:

* <font style="color: red;">RED: O teste falha.</font>
* <font style="color: green;">GREEN: O teste passou.</font>
* <font style="color: blue;">REFACTOR: Otimizar o código escrito.</font>

<img src="{{ site.url }}/public/img/what_is_tdd/tdd.png" alt="">

## Download

Hydejack is developed on and hosted with GitHub. Head to the [GitHub repository](https://github.com/qwtel/hydejack) for downloads, bug reports, and feature requests.

## Sidebar
I love the original Hyde theme, but unfortunately the layout isn't as great on small screens.
Since the sidebar moves to the top, the user has to scroll just to read the title of a blog post.

By using a drawer component I was able to retain the original two column layout. It's possible to move the drawer via touch input (with the help of a little JavaScript).

Since the background image contributes to the feel of the page I'm letting it peek over the edge a bit. This also provides a hint to the user that an interaction is possible.

### Preview
{:.preview}

<iframe class="preview" src="/anchietajunior.github.io/2016/08/26/what-is-tdd/" style="border: 1px solid #ddd; width: 340px; height: 520px; margin-top: 1rem"></iframe>

## Manual

### Configuration
You can configure important aspects of the theme via [`_config.yml`](https://github.com/qwtel/hydejack/blob/master/_config.yml). This includes:

* the blog description in the sidebar
* the (optional) author description and photo
* default image and link color of the blog
* the github and twitter usernames

### How to Change the Image and Color of a Post
In the manifest of a blog post, simply add an url as `image` and a CSS color as `color`:

~~~yml
layout: post
title: Introducing Hydejack
image: http://qwtel.com/hydejack/public/img/hyde.jpg
color: '#949667'
~~~

### How to Add a New Tag

Tags are not meant to be used #instagram #style: #food #goodfood #happy #happylife #didimentionfood #yougetthepoint, as each tag requires some setup work. I tend to think of it as categories that can be combined.

1.  Add an entry to `_data/tags.yml`, where the key represents a slug and provide at least a `name` value and optionally `image`, `color` and `description`.

    Example `/_data/tags.yml`:

    ~~~yml
    mytag:
      name: My Tag
    ~~~

2.  Make a new file in the `tag` folder, using the same name you've used as the key / slug and change the `tag` and `permalink` entries.

    Example `/tag/mytag.md`:

    ~~~yml
    layout: blog_by_tag
    tag: mytag
    permalink: /tag/mytag/
    ~~~

3.  Tag your blog posts using the `tags` key (color and image will only depend on the first tag).

    ~~~yml
    layout: post
    title: Introducing My New Tag
    tags: [mytag, othertag]
    ~~~

4. (optional) Add the tag to the sidebar, by adding it to `sidebar_tags` in `_config.yml`.
   They will appear in the listed order.

   ~~~yml
   sidebar_tags: [mytag, othertag]
   ~~~

[tag]: http://www.minddust.com/post/tags-and-categories-on-github-pages/
