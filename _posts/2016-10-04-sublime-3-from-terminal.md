---
layout: post
title: Como executar o Sublime Text 3 via terminal Mac
tags: [sublime 3, mac, terminal]
color: 'blue'
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

Hoje passando só pra deixar uma dica pra quem utiliza o Mac OS X (El Capitan 10.11) e quiser executar o sublime direto do terminal ou iterm, o que na minha opinião é muito prático e produtivo.

Apenas execute o comando no terminal:

```
ln -s "/Applications/Sublime Text.app/Contents/SharedSupport/bin/subl" /usr/local/bin/sublime
```

Certifique-se de que foi executado com sucesso executando o seguinte comando dentro de um diretório de algum projeto:

```
sublime .
```

Tudo ok? Então, valeu!