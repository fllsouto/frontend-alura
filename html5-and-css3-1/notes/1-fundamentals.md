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











