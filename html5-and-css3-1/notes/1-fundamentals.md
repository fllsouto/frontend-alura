## Fundamentals

- O navegador consegue "abrir" e "ler" arquivos HTML
- O HTML **formata conteudo**
- Ao marcar um conteudo com uma certa **tag** eu posso afrupar coisas. Títulos terão sempre a mesma cara, subtítulos também, e assim por diante
- Tags passam informações para o navegador

```HTML
<meta charset="utf-8">
//charset é um atributo da tag e define qual a codificação de caracter está sendo utilizada na página
```
### Estrutura básica do HTML

```HTML
<!DOCTYPE html>
//Diz para o navegador exatamente qual versão do html está sendo utilizada, neste caso não está explícito então
//assume-se que seja a mais recente (HTML5)
<html>
  //Delimitação do início do documento
  <head>
  	//Guarda metainformações (informações para o navegador)
  <head>
  <body>
    //Guarda o conteudo da página
  </body>
<html>
```
### Estilo

Separa o HTML do CSS da maior unidade ao estilo, as coisas ficam mais desassociadas. 

#### Formas de utilizar a tag style

```HTML
//Direto na tag
<h1 style="font-size: 60px">Título</h1>


<head>
  //Declarado dentro da tag head, aplicado direto no elemento **h1**
  <style>
  	//seletor { regra }
    h1 {
      font-size: 60px
    }
  </style>
</head>

<head>
  //Separado em um arquivo externo
  <link rel="stylesheet" href="estilo.css">
</head>
```

#### Definindo cor
rgb(255, 10, 12) ou #FF0A0C
#### Definindo fonte
font-family: "Open Sans", "Arial"

Esse estilo define qual fonte será utilizada, caso ela não exista no navegador do usuário a seguite da lista é tentada, **indo da esquerda para a direita**. Posso definir uma fonte "qualquer" de um tipo específico, por exemplo **Sans-Serif**

#### Links de conteúdo
```HTML
//Cria uma "ancora" na palavra taggeada
<a href="www.example.com">exemplo</a>

//Essa tag insere uma imagem na tela. Ela não precisar ser fechada e o atributo alt é utilizado para prover acessibilidade para leitores de tela e informar para robôs de busca do que se trata a imagem.
<img src="eu.png" alt="foto do joão da silva">
```

#### Navegação
```HTML
//A tag nav da semântica ao documento, dizendo que aquela lista é usada para navegação do site. Isso é util para correta indexação do site por ferramentas de busca.
<nav>
  <ul>
    <li> ... </li>
    <li> ### </li>
    <li> @@@ </li>
  </ul>
</nav>
```

#### HTML Semântico
Informações bem descritas sobre a página

#### Hierarquia de seletores

```HTML
//Com o espaço eu consigo selecionar hierarquicamente a qual seletor eu quero aplicar um dado estilo
main h1 {
	
}
```
#### Entidades HTML
São úteis para caracteres especiais : **&copy = ©**

#### Redirecionamento

Dado que estou no endereço http://www.meusite.com/blog.html se eu clicar no link abaixo o navegador irá mudar apenas o final da URL, isso se chama **link relativo**
```HMTL
<a href="portifolio.html">Meu Portifólio</a>
```
Um **link absoluto** é uma URL completa. Posso ter links relativos em hierarquicas
- /portifolio.html
- /post/html5-e-css3.html

#### [Box Model](https://developer.mozilla.org/pt-BR/docs/Web/CSS/box_model)
Padding : Espaçamento do texto/conteudo para a caixa onde ele está contido.

Border : Cria uma borda na caixa de texto. Seus parâmetros são: **o tamanho da borda, o tipo do tracejado e a cor.**

Quando definimos um width para o conteudo para o conteudo nem sempre pode ser calcuado da forma que esperamos. Pode ser necessário aplicar uma regra **box-sizing: border box** para dizer que todos aqueles elementos somam o nosso width

```
main div {
	width: 750 px;
  margin: 0 auto;
}
// <--Auto-->|--div[750]--|<--Auto-->
```

- O navegador aplica estilos por default na página
- Eu posso definir um arquivo **reset.css** que irá servir como base do estilo. Esse arquivo remove a maioria dos estios deifnidos pelos navegadores Isso forece um ponto de partida consistente para definir outros CSS
- O navegador importa o CSS na ordem que está definido no **Head**. Nessa sequência acontece também a sobrescrita dos estilos. O navegador pode sobrescrever pela **especificidade** também.






