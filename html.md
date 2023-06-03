# HTML

Atributos: características

- id: identificador do elemento

<h1> título 
<p> parágrafo
<blockquote> citação

<strong> negrito
<i> itálico
<u> underline
<mark> marca texto
<sub> sobrescrito
<ol> lista ordenada
<ul> lista não ordenada
<li> item de lista

#### Formulários

<form> formulário
-atributo action: colocar o endereço do servidor para onde os dados serão enviados
-atributo method: post (não manda pela url, mas sim via body da requisição para servidor, sem aparecer no endereço)
-atributo method: get (o que foi digitado no formulario vai aparecer na url)
-atributo target: abrir na mesma aba ou não (_blank)
-atributo name: nome do formulário
-atributo autocomplete: autocompleta os dados com aqueles que foram armazenados //on=autocompleta off=não autocompleta
- on(algumacoisa): muito urilizado no javascript - evento
<input> coloca o campo na tela // type: text, number, password
<button> coloca botão // submit


##### Input e tipos


type="text" : campo texto
type="number" : campo número // aceita min="" ; max="" ; step=""
type="button" : campo botão
type="color" : caixa de diálogo de cor
type="email" : solicita um email
type="range" : cria um "scroll
type="date/week/month" : calendário para data
type="url" : solicita uma url
type="checkbox" : caixa de seleção // aceita mais de uma seleção
type="radio" : caixa de seleção // um ou outro // colocar name="aceita"

type="hidden" :
type="file" : campo enviar arquivos // multiple para aceitar vários arquivos
type="search" : campo de busca // aparece um "x" no final para limpar a busca


##### Checkbox e radio

checkbox: uma variável com diversos valores // para fazer enviar como lista para o backend, colocar name="opcional[]" e no <form method="post"> //
radio: para selecionar um ou outro, colocar name="" value=""
disable: desabilita a opção


##### Button

button: aplicar "on" pelo javascript
reset: limpar os campos do formulário em que está incluído
submit: enviar o formulário (o enter do teclado é o submit no formulário, por isso deve estar dentro da tag <form> para que seja validado antes de enviar)


##### Select

select box: lista pré-definida de valores que se quer que o usuário escolha // selected: pré-selecionado para aparecer // multiple: selecionar mais de um
<select name="role">
    <option value="">
    <option value="">
    <option value="">
    <option value="">



##### Textarea

dá para definir rows e columns para deixar fixo



#### Estruturação do HTML e formatações

<sup>: caractere "elevado"
<sub>: caractere "abaixado"
<strong> ou <b> para acessibilidade é melhor a ênfase do strong
<fonte color="" face=""> cor, fonte(letras) 


##### Tags div e span

são utilizadas para estruturar o HTML

<div> estruturar o site por "seções", criando espaços para cada item //formatação rápida: ex: ul>li*3>a**
<span> por padrão, não possui formato block e ajuda na estilização do texto quando se quer fazer algo com o css (possui o mesmo intuito da div, mas com formatação diferente e esem quebrar o texto, facilitando a formatação)



##### Tag fieldset

tag auxiliar, que encapsula o conteúdo
utilizada junto com a tag <legend>

<fieldset>
    <legend>
        <div>
            <label> <input>


##### Tag embeds e iframes

<embed> tag não mais utilizada, mas era utilizada para carregar uma mídia
<iframe> tag que coloca um site dentro de outro site, mantendo atualizado... além de mídias como o <emded>, carrega videos e outros sites tbm


#### Mídias


##### Imagem
<img src=""> aceita formatos:
- gif
- png (melhor que jpg, e é possível conseguir transparência - utilizar em caso de logotipo)
- jpg (perde muito em resolução e outros - utilizar em galeria de imagem)
- svg (vetorial, pegando as coordenadas da imagem - melhor, mas limitado - consegue dimensionar a img sem perder a resolução)

<svg> melhor do que a tag img no caso do arquivo svg


###### Atributos

title="" define o título da imagem para o usuário quando passar o mouse por cima
alt="" bom para a acessibilidade, definindo uma "tradução da imagem" ou descrição 


##### Áudio

evolução da embed, sendo exclusivo pra som

<audio src=""> aceita formatos:
- mp3

###### Atributos
autoplay
controls


##### Vídeo

<video src=""> aceita formatos:
- mp4
- webm

##### Track

auxiliar da tag <video>, sendo a legenda

<track src=""> aceita formatos:
- mp3

###### Atributos
kind=""

    -captions
    -chapters
    -descriptions
    -subtitles

srclang="" língua falada
    uso do defaut, que seria uma escolha de padrão assim que o video começar



#### Tabelas

<table cellspacing="espaçamento entre células - já vem por padrão (eliminar caso for editar no css)" cellpadding="espaçamento entre borda e conteúdo" summary="descrição do assunto da tabela">
    <tr>
        <td></td> -----> <th></th>
        <td></td> -----> <th></th>
    </tr> // cada conjunto deste é uma linha da tabela e cada td é uma coluna
    <tr>
        <td></td>
        <td></td>
    </tr>


Tabelas devem ter o nome mais curto possível, e no atributo title coloca-se a descrição, ficando assim melhor para visualizar
tbody, thead e tfoot mesmo quando fora de ordem no doc html, ficam ordenados na página sequencialmente

##### tr
linha da tabela que comportam os td's
comporta o id="number" para achar uma linha específica



##### td
coluna da tabela dentro do tr


##### th
no lugar do td, define que é o cabeçalho da tabela

##### tbody
corpo da tabela - "td"

##### thead
cabeça da tabela - "th"


##### tfoot
rodapé da tabela - "último td"

##### caption
descrição da tabela - nome da tabela
diferente do summary, que não aparece para o usuário final, mas é lido através de um programa de acessibilidade - é tbm uma descrição do resumo dos dados da tabela, não só o nome da tabela


#### Estilização da Tabela no CSS

table { border, background-color, color, border}


no css: table tr:nth-child(even) {estilização, zebrado}
no css: table tr:nth-hover(even) {estilização, linha fica de outra cor quando o mouse está por cima}
box shadow generator

mesclagem de células: colspan="" ou rowspan="" (coluna ou linha)