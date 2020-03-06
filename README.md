# aula-06_03_2020
Pesquisa sobre CSS
# CSS Conceitos e Aplicações
O Cascading Style Sheets (CSS) é uma "folha de estilo" composta por “camadas” e utilizada para definir a apresentação (aparência) em páginas da internet que adotam para o seu desenvolvimento linguagens de marcação (como XML, HTML e XHTML). O CSS define como serão exibidos os elementos contidos no código de uma página da internet e sua maior vantagem é efetuar a separação entre o formato e o conteúdo de um documento.
### Inline: aplicadas a um elemento específico num documento.
### Internal: definidas num documento específico. Permitem aplicar o estilo apenas a esse documento.
### External: definidas num ficheiro externo e associadas a vários documentos HTML.
# SELETORES
### Seletor universal
Os conteúdos de cada um dos elementos da marcação, ao serem renderizados em um navegador, são estilizados com regras CSS mínimas (por exemplo: cor e tipo de fonte, margens, paddings, etc.) que fazem parte de uma folha de estilos nativa do navegador e que na ordem de cascata tem a prioridade mais baixa, ou seja, qualquer declaração de estilo do autor ou usuário sobrescreve a folha de estilos nativa.
Não existe uma padronização para essa folha de estilos e cada navegador implementa sua própria folha de estilos nativa. Como consequência ocorrem inconsistências de renderização, em relação a estilização básica, entre navegadores.

Destas inconsistências a que produz maiores transtornos é a não padronização dos valores para as propriedades margin e padding.

A principal utilização do seletor universal é "zerar" essas propriedades para todos os elementos da marcação. Como consequência o autor terá que definir explicitamente para cada elemento, na sua folha de estilos, aqueles valores.
## Ex:
* {
  margin: 0;
  padding: 0;
  }
  ### Seletor tipo 
  Sintaxe: E
Usado para estilizar os elementos da marcação que são de um mesmo tipo; por exemplo: elemento do tipo p (parágrafo), do tipo div, do tipo ol, do tipo strong, e assim por diante.
## Ex:
i { color: orange }
   ### Seletores de atributo
   Combina elementos baseado no valor de um atributo dado.
   
[attr]
    Representa um elemento com atributo de nome attr.
[attr=value]
    Representa um elemento com um atributo de nome attr, o qual o valor é  exatamente  value.
[attr~=value]
    Representa um elemento com um atributo de nome attr, o qual value é  uma lista de palavras separadas por espaços, e uma dessas é  exatamente  value.
[attr|=value]
    Representa um elemento com um atributo de nome attr  o qual o valor pode ser exatamente value ou pode começar com value imediatamente seguido por hífen - (U+002D). Isso somente é usado para linguagens que combinam sub-códigos.
[attr^=value]
    Representa um elemento com um atributo com nome attr que tem um valor prefixado (precedido) por value.
[attr$=value]
    Representa um elemento com um atributo de nome attr que  tem como sufixo (seguido) por value.
[attr*=value]
    Representa um elemento com um atributo de nome attr o qual valor contém ao menos uma ocorrência de value contido na string.
[attr operator value i]
    Adiciona um i (ou I) antes do fechamento das chaves {}, faz com que o valor seja comparado sem levar em conta caixa alta ou caixa baixa(para caracteres dentro da faixa ASCII). 
   ### Seletores do tipo peseudo-classe
## Elemento raiz
 Casa com o elemento raiz do documento.
 Sintaxe: :root
 ## Ex:
:root { color: blue; }
## Enésimo filho
Casa com o elemento que é o enésimo filho do seu elemento pai
Sintaxe: E:nth-child(n)
## Ex:
li:nth-child(4) { color: red; }
li:nth-child(2n+1) { color: blue; }
li:nth-child(5n) { color: green; }
## Enésimo filho de trás para frente
Casa com o elemento que é o enésimo filho do seu elemento pai, contado de trás para frente na marcação
Sintaxe: E:nth-last-child(n)
## Ex:
li:nth-last-child(3n) { color: salmon; }
### Seletor classe
Casa com o elemento que tem determinado valor para o atributo classe
Sintaxe: E.foo
## Ex:
.um { background: moccasin; }
### Seletor ID
 Casa com o elemento que tem determinado valor para o atributo id
Sintaxe: E#foo
## Ex:
#dois { background: honeydew; }
### Seletor descendente
 Casa com o elemento que descende de determinado elemento
Sintaxe: E F
## Ex:
div.um i { color: crimson; } 
div.dois * * i { color: orangered; } 
### Seletor filho
 Casa com o elemento filho de determinado elemento
Sintaxe: E>F
## Ex:
.um > i { color: red; }
.dois > p > i { color: blue; }
.dois > div > p > i { color: orange; }
### Seletor que imediatamente sucede
 Casa com o elemento irmão que imediatamente segue-se a determinado elemento
Sintaxe: E+F
.um p + div { border: 1px solid navy; background: lightpink;}

.dois p + div p + p { border: 1px solid navy; background: lightsalmon;}
### Seletor que sucede
 Casa com o elemento irmão que segue-se a determinado elemento
Sintaxe: E~F
## Ex:
.um p ~ i { color: red; }

.dois p + div i ~ p { color: blue; }
### Referência CSS local (na página):

## Interno: 
Estilos CSS feitos desta forma são carregados cada vez que um site é atualizado, o que pode aumentar o tempo de carregamento. Além disso, você não poderá usar o mesmo estilo CSS em várias páginas, pois está contido em uma única página. Mas a vantagem disso é que ter tudo em uma página facilita o compartilhamento do modelo para uma visualização.

## Externo: 
Esse método pode ser o mais conveniente.Tudo é feito externamente em um arquivo .css. Isso significa que você pode fazer todo o estilo em um arquivo separado e aplicar o CSS a qualquer página desejada. O estilo externo também pode melhorar o tempo de carregamento. 

### Framework’s CSS mais usados:


## Bootstrap:
Entre suas vantagens, podemos citar a documentação farta e a comunidade muito ativa, a infinidade de componentes que podem ser facilmente chamados em suas aplicações, além da boa base de padrões estéticos, que permitem criar páginas belas e funcionais.

## Purecss:
Ele trabalha somente com códigos HTML e CSS puros, fazendo com que as aplicações sejam leves e fáceis de serem entendidas pelos programadores. Outra vantagem é que o framework é modular, ou seja, é possível importar somente as classes que possuem os códigos que você precisa, ou importar o framework completo. Isso dá uma autonomia maior ao desenvolvedor.

## Foundation:
O Foundation tem a vantagem de manter um código enxuto e conciso, além de estar adaptado para os diferentes tipos de tela.




