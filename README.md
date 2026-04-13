# HTML

## O que é HTML - HyperText Markup Language (Linguagem de Marcação de Hipertexto)
Como o nome já indica, HTML não é uma linguagem de programação, e sim uma linguagem de marcação. Ele serve para organizar a estrutura de uma página web. Isso muitas vezes acaba sendo visto como a “parte visual”, mas na prática o papel dele é outro: ele organiza o conteúdo para que qualquer tipo de usuário consiga acessar e entender a informação, inclusive pessoas com deficiência.

Por isso, a forma como o HTML é estruturado tem impacto direto na acessibilidade e na usabilidade de um site.

O HTML é formado por vários elementos, e cada um deles é definido por uma tag, que funciona como uma espécie de marcador indicando o tipo de conteúdo e o seu papel dentro da página. Por exemplo, `<h1>` representa títulos principais, `<p>` é usado para parágrafos, `<a>` cria links, entre outros.

Além disso, as tags podem receber atributos, que são informações extras que ajudam a detalhar ou modificar o comportamento dos elementos, como `class`, `id`, `src` e outros.

IMPORTANTE:HTML é uma linguagem de marcação, usada basicamente pra organizar o conteúdo de uma página. Em algumas buscas você vai ver tags como `<b>` e `<i>` sendo usadas pra deixar texto em negrito ou itálico.

Só que hoje em dia existe um jeito mais “correto” de fazer isso, usando `<strong>` e `<em>`. A diferença é que essas duas não servem só pra mudar a aparência do texto, elas também carregam significado.

Na prática, `<strong>` indica que algo é importante, e <em> dá uma ideia de ênfase. Isso ajuda não só na forma como a página é lida por pessoas, mas também por leitores de tela e outras ferramentas de acessibilidade.

Já `<b>` e `<i>` acabam sendo só visuais mesmo, sem esse peso de significado. Por isso, sempre que der, é mais interessante usar as versões semânticas.

## Tags
As tags são as “etiquetas” do HTML. Elas dizem o que cada parte do conteúdo é deixando mais facil de definir e mudar futuramente.

```html
<p>Isso é um parágrafo</p>


<title>isso é um titulo</title>

```

## Cores,Fontes e etc.
```html
<p class="banana12">Isso é um paragrafo com classe banana12</p>
```
Bom lembrar que as classes nao podem começar com numeros

e com cores seria assim:
```html
<P style="color: red;">isso é um paragrafo vermelho</P>
 ```
 e com fonte strong(negrito) é assim:
 ```html
 <strong>Isso é um paragrafo em negrito</strong>
 ```
 ## Utilizar stylesheet é uma boa pratica?
Bom, como voce viu nas tags anteriores, cada tag que tinha um estilo proprio tinha "style" na sua construçao, mas e se voce quiser simplesmente diminuir ou deixar mais organizado o seu codigo? Voce simplesmente cria uma STYLESHEET, eu considero uma boa pratica pois ajuda a organizar e facilita a modificaçao de textos. Para criar um stylesheet, voce deve utilizar a tag link,
no vscode ou no codespace do github o auto-preenchimento ja vai recomendar algo assim:`<link rel="stylesheet" href="style.css"> `
e é exatamente isso oque voce precisa. No "href"style.css", "style" é o nome do nosso stylesheet que pode ser mudado para qualquer coisa des de que siga as regras para nomeamento de arquivos e de boas praticas, ".css" é  a extensao obrigatoria caso o arquivo seja css

 É interessante saber que oque mostrei aqui é apenas o inicio do html apenas o mais simples do simples, e que caso voce realmente queira seguir no ramo de webdesign ou construçao de sites, voce precisara saber bem mais doque isso

## Estrutura basica de um documento em html
Todo arquivo HTML começa com `<!DOCTYPE html>`, que informa ao navegador que o documento está usando HTML5
Depois disso, a estrutura principal é dividida em duas partes: `<head>` e `<body>`

`<head>`

É onde ficam as informações da página que não aparecem diretamente na tela, mas são importantes para o funcionamento do site e tambem contém metadados, como título, links de CSS, scripts e informações que o navegador usa para interpretar a página.

## Atributos HTML
Os atributos HTML servem para adicionar informações extras aos elementos. Eles são escritos dentro da tag de abertura e seguem sempre o formato nome="valor".

Eles ajudam a definir propriedades como comportamento, aparência ou funcionamento de um elemento.

Exemplos comuns:

href define o destino de um link
src define a origem de uma imagem
alt descreve uma imagem
Exemplo com link

A tag `<a>` é usada para criar links, e o atributo href indica para onde o usuário será direcionado.

<a href="https://www.google.com">Visite o Google</a>

Nesse caso, o texto “Visite o Google” aparece na página como um link clicável. Ao clicar, o usuário é levado para o site do Google.
## Esse foi o codigo usado:`<a href="https://www.google.com">Visite o Google</a>`
## Lista de todas as tags HTML
Neste link, você pode encontrar uma lista completa de todas as tags HTML, juntamente com suas descrições e exemplos de uso: MDN Web Docs - Elementos HTML ou W3Schools - HTML Tags.
<a href="https://www.w3schools.com/TAGS/default.asp">Visite w3schools</a>
 
 # CSS - Cascading Style Sheets (Folhas de Estilo em Cascata)
 CSS é uma linguagem de estilo usada para definir a aparência de uma página web. Enquanto o HTML organiza o conteúdo, o CSS cuida de como esse conteúdo vai ser exibido.

Com ele, é possível controlar cores, fontes, espaçamentos, margens, tamanhos e o layout da página como um todo.

Uma das principais ideias do CSS é separar estrutura e estilo. Ou seja, o HTML fica responsável pelo conteúdo e o CSS pela parte visual. Isso deixa o código mais organizado e fácil de manter.

## Como o CSS funciona
O CSS é formado por seletores e declarações:

Seletores: escolhem quais elementos HTML vão receber o estilo
Declarações: definem as regras de estilo (propriedade e valor)

## Exemplo basico com stylesheet
`<p>banana</p>`
 `p {
    color: red;
 }`

## Como ficam as coisas sem CSS?
Ficam no estilo padrao do navegador se mantendo de acordo com configuraçoes do navegador do usuario

## Seletores 
Os seletores CSS servem para escolher quais elementos HTML vão receber estilos. Eles funcionam seguindo a estrutura do HTML (tipo uma “cascata”), então dá pra selecionar elementos específicos ou grupos usando tipo, classe, ID, atributos e posição.

Exemplo básico:

Tipo: p { } muda todos os parágrafos
Classe: .titulo { } muda tudo com essa classe
ID: #paragrafo1 { } muda só um elemento específico
Atributo: a[href="#"] { } muda links com certo valor
Pseudo-classe: p:first-child { } muda um elemento em uma situação específica

Também dá pra selecionar pela hierarquia do HTML:

Descendente: main section p pega parágrafos dentro de section dentro de main
Filho direto: main > section pega só filhos diretos
Irmão adjacente: h1 + p pega o primeiro parágrafo depois do h1
Irmão geral: h1 ~ p pega todos os parágrafos que são irmãos do h1


