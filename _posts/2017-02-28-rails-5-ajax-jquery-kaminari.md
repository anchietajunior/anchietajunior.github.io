---
layout: post
title: Ajax, JQuery, Rails 5 e Kaminari
tags: [ajax, jquery, rails5, kaminari]
color: 'orange'
---

<style>
  .preview {
    display: none;
  }

  @media (min-width: 48em) {
    .preview {
      display: block;
    }
</style>

E ai, já sentiu aquela necessidade de implementar alguma coisa que utilize **Ajax** em sua aplicação Rails e ficou com aquela impressão de que "isso ta estranho" ou "isso não vai funcionar"?

Seus problemas "se acabaram-se"... brincadeira, não acabaram, mas este post que vos apresento hoje tem o propósito de servir como referência caso precisem (inclusive eu quando esquecer, não me lembro de tudo, minha idade já não me permite esta façanha).

Estou partindo do princípio que o conceitos de **Ajax**, requisições assíncronas e Rails estão bem entendidos por parte do leitor.

Bom, pretendo deixar bem explicado aqui dois exemplos de requisições assíncronas, através de um "click" carregar mais elementos em uma página, ou implementar um **infinite scroll**, que se utilizam das mesmas requisições mas de maneira diferente agem na página no qual estão presentes.

Criando, configurando e populando a aplicação:

```sh
$ rails new ajaxapp -T -B
```

Adicione as gems **Kaminari** e **Faker** ao Gemfile:

```ruby
gem 'kaminari'
gem 'faker'
```

Instalando as dependências:

```sh
$ bundle install
```

Gerando o scaffold dos posts e migrando para o banco:

```sh
$ rails generate scaffold Post title:string content:text
```

```sh
$ rails db:migrate
```

No nosso seeds.rb:

```ruby
50.times do |post|
  Post.create!(title: Faker::Lorem.sentence, content: Faker::Lorem.paragraph)
end
```

Populando o banco com as seeds:

```sh
$ rails db:seed
```

Agora temos nossa app configurada e populada, agora iremos tratar de fato o **Ajax**.



<!--
```html
<html>
	<head></head>
	<body></body>
</html>
```

```ruby
def diga_oi
	puts "oi"
end
```

```css
.header {
	border-top: 1px solid #333;
	border-radius: 5px;
}
``` -->
