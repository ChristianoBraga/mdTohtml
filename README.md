# MD para HTML

Trabalho para a disciplina de Linguagens Formais, 2021.1

## Objetivo

Exercitar o uso de expressões regulares.

## Tarefa

Implementar um tradutor de uma simplificação da linguagem Markdown para HTML em Python 3 utilizndo o pacote PLY.

## Preparação

* Instale Python 3 com o pacote PLY. 
  - Com Python 3 instalado no seu sistema, execute `$ pip3 install PLY`.

## A linguagem Markdown simplificada 

- Permite a escrita de documentos como por exemplo:
```
# Teste header 1

## Teste header 2

**teste** **bold**

_teste_ _italico_

- teste itemizacao 1
- teste itemizacao 2

1. teste enumeracao 1
1. teste enumeracao 2

teste paragrafo 1, teste paragrafo 2

[teste link Google](http://www.google.com)
```

- A tradução para HTML deve produzir:
```
   The [6]current development sources have the latest version of Lynx
<html>
<h1>Teste h1 </h1>
<p>
<h2>Teste h2 </h2>
<p><strong>teste</strong> <strong>bold</strong>
<p><em>teste</em> <em>italico</em>
<p>
<ul>
<li>teste itemizacao 1 </li>
<li>teste itemizacao 2 </li>
</ul>
<p>
<ol>
<li>teste enumeracao 1 </li>
<li>teste enumeracao 2 </li>
</ol>
<p>teste paragrafo 1, teste paragrafo 2
<p><a href="http://www.google.com">teste link Google</a>
</html>
```

- Os elementos de Markdown simplificado são
1. Headers: linhas começadas com `#`. A tradução de `#` para HTML é `h1`, de `##` é `h2` e assim sucessivamente.
2. Palavras em negrito e itálico. O texto `**texto**` é traduzido em `<b>texto</b>` e `_texto_`.
3. Parágrafos. Uma linha em branco inicia um parágrafo. 
4. Itemizações. Linhas iniciadas com `-` determinam um item numa lista não-ordenada em HTML. Por exemplo, o texto Markdown abaixo     
   ```
   - Isto é um item.
   - E isto também.
   ``` 
   deve ser traduzido ao código HTML abaixo.
   ```
   <ul>
   <li>Isto é um item.
   <li>E isto também.
   </ul>
   ```





