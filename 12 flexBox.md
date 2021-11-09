# BootCamp Impulso React Developer
## Introdução ao Curso
### Apresentação do curso
Apresentar os fundamentos e aplicações da propriedade flex box;
Requesitos: HTML5 e CSS3. editor e navegador.
etapa 1 - introdução ao FlexBox
etapa 2 - fundamentos do FlexBox
etapa 1 - projeto integrador
### Proposta de projeto final
Projeto real de uma landinpage real que pode compor o portifolio de projetos nosso;
### Introdução ao Flex Box
conhecer a estrutura basica do flexbox, diferenciar Flex Container e Flex Item; e inicialmente conhecer algumas propriedades;

Foi projetado como um modelo de layout unidimensional (ele mantém um comportamento adaptativos a diversas situações, plataformas e tamanhos[flexível]);

flex container = a tag que que envolve os itens sobre a qual aplicamos a propriedade "display:flex", transforma todos os seus itens filhos em 'flex itens'.
se aplica a div, span h1, h2, a 
propriedades relacionadas:

- display; inicializador do container
- flex-direction; fazer o direcionamento dos itens (linha, coluna...)
- flex-wrap; aplicado a quebra ou não de linha
- flex-flow; uma abreviação para o direction e wrap
- justify-content; alinha os itens do container de acordo com sua direção
- align-items; alinha os itens de acordo com seu eixo no container
- align-content; alinha as linhas desse container

flex item - são os filhos diretos do flex container e podem se tornar flex containers também (aplicando-se a propriedade display) e saiba que isso é recursino podendo ter diversas camadas;

propriedades relacionadas(flex item)
- flex-grow; definir o fator de crescimento.
- flex-basis; definir o tamanho inicial desse item antes da distribuição dos espaço restante dentro do container.
- flex-shrink; define a capacidade de redução.
- flex; é um abreviação para as três propriedades citadas acima.
- order; ordem de distribuição e listagem desses items.
- align-self; definir alinhamento de um item específico dentro desse container.
## Fundamentos do FlexBox - Parte 1
### Estrutura básica do display:flex
Existe uma grande lista de propriedades a serem trabalhas, porém estão distribuidas na aplicaçãos ao 'flex container(elemento inicial)' ou 'flex item(elemento filho)'

vscode extensões: HTML Snippets e Live HTML Previewer.

agora estamos focados nas propriedades do 'flex container'

conhecer e aplicar a propriedade de inicialização do flex container que é a base de toda construção do nosso curso;

- display flex: Torna a tag um elemento do tipo flex container e assim os filhos diretos da tag tornam-se automaticamente flex items, essa propriedade pode ser aplicada basicamente em qualquer tag html inclusive os links;

### Prática com display:flex
.flex
    max-width: 300px;
    padding: 10px;
    border: 2px solid black;
.item
    background-color: aqua;
    margin: 5px;

aplicada a propriedade display:flex cada elemento passa a ocupar o máximo de seu conteúdo e se abrigar dentro do container respeitando a orientação em linha (o que pode ser mudado posteriormente); é comum ser utilizado o mobile nos menus que são capazes de se adaptarem às telas e respeitem a proporcionalida do dispositivo; em caso de haver muitos itens acontece vazamento o que deve ser tratado;

### Estrutura básica do flex direction
entender o comportamento padrão de orientação horizontal de um flex container e aprender a modificar essa orientação horizontal;

É a propriedade que estabelece o eixo principal do container, definindo assim a direção que os flex items são colocados no flex container; [linha ou coluna];

#### os eixos
row(padrão): à direção do texto, esquerda para direita. 1 2 3 4
row-reverse: sentido oposto à direção do texto. 4 3 2 1

column ordenação de cima para baixo, em coluna unica(de cima para baixo)
column-reverse: ordenação inversa (de baixo para cima)
### Prática com flex direction
È muito comum nós necessitarmos mudar a orientação dos nossos elementos em tela quando trabalhamos com break points (dimensões de telas) diferentes. Onde podemos mudar de linha pra coluna quando estivermos cuidando da responsividade é um problema que o flex Container surge pra resolver, tratando individualmente os elementos;

### Estrutura básica do flex-wrap
É a propriedade que define ou não a quebra de linha no nosso container.
Por padrão eles não quebram linhas, isso faz com que os flex itens sejam compactados além do limite do conteúdo;

 - nowrap: é o padrão, não permite a quebra de linha;
 - wrap: permite a quebra de linha assim que um dos flex itens não puder mais ser compactado;(evita vazamento).
 - wrap-reverse: permite a quebra de linha assim que um dos flex itens não puder mais ser compactado, porém na direção contrária da linha, acima (pra cima)!

### Prática com flex wrap

### Estrutura básica e prática com flex-flow
É um atalho para duas propriedades vistas anteriormente: flex-direction e flexwrap. Porém seu uso não é tão comum, visto que, quando mudamos o flex-direction para column, mantemos o padrão do flex-wrap que é nowrap.

### Estrutura básica do justify content
Essa propriedade vai se encarregar de alinhar os itens dentro do container de acordo com a direção pretendida e tratar da distribuição de espaçamentos entre eles.
OBS: se temos itens que ocupam 100% do container essa propriedade não se aplica;
- flex-start: início do container.
- fles-end: final do container, respeitando o limite do conteúdo.
- center: traz todos elementos ao centro do container.
- space-between: cria um espaçamento igual entre os elementos, pega o primeiro elemento e coloca muito proximo ao inicio do container (próximo à borda esquerda); e o elemento final é levado ao final do container à direita;
- space-around: os espaçamentos do meio são duas vezes maiores que o inicial e final(esse não cola nas bordas).
left, rightm etc; más os que aqui estão são os principais quando falamos de flexBox! Ou seja, nem todas as propriedades são aplicadas ao flexBox!
### Prática com justify-content - Parte 1
OK Made in row;
### Prática com justify-content - Parte 2
OK Made in column;
### Estrutura básica e prática com align-items
align-items - Trata do alinhamento dos flex itens de acordo com o eixo do conteiner. O alinhamento é diferente para quando os itens estão em colunas ou linhas. Permite o alinhamento central no eixo vertical.
no justify-content não aplicamos o conceito de altura no item, mas aplicamos no container, aqui não será aplicado pois será trabalhada a proporcionalidade e expande os elementos crescendo;
TIPOS DE ALINHAMENTOS
- center: alinhamento dos itens ao centro;
- stretch: padrão, e os flex itens cresçam igualmente (conteúdo do maior);
- flex-start: alinhamento dos itens no início;
- flex-end: alinhamento dos itens no final;
- baseline: alinhamento de acordo com a linha base da tipografia dos itens;

### Estrutura básica e prática com align-content
Esta propriedade se responsabiliza por tratar o alinhamento das linhas do container em relação ao eixo vertical do container.
Precisamos que sejam respeitadas algumas orientações:
    1. O Container utilize quebra de linhas;
    2. A altura do container seja maior que a soma das linhas dos itens;

TIPOS DE ALINHAMENTO

- center: alinhamento dos itens ao centro;
- stretch: é o padrão e os flex itens crescem igualmente;
- flex-start: alinhamento dos itens no início do container (eixo vertical) comprime pra cima;
- flex-end: alinhamento dos itens no final (comprime pra baixo);
- space-between: cria um espaçamento igual entre os elementos;
- space-around: os espaçamentos do meio são duas vezes maiores que o início e final (gruda nas extremidades e deixa pequeno espaçamento);
mescla de conceitos que já vimos anteriormente em: 'justify-content', 'align-items';

**está foi a última propriedade aplicada aos flex container's**

## Fundamentos do FlexBox - Parte 2
### Estrutura básica e prática com flex grow
Define a proporcionalidade de crescimento dos itens, respeitando o tamanho de seu conteúdos internos;
OBS: Não irá funcionar caso tenhamos adicionado 'justify-content' ao nosso flex container. 

flex-grow: (0,1,2,3)[espaço ante e depois do conteúdo do flex item]
quando aplicado justify-content ao container só funcionou onde o grow era '0'
### Estrutura básica do flex-basis
relação com flex itens...
É a propriedade que estabelece o tamanho inicial dos itens antes da distribuição do espaço restante dentro dele, usando como base o conteúdo interno disposto.
VALORES POSSÍVEIS:
- auto: caso o item não tenha tamanho, este será proporcional ao conteúdo do item.
- px, %, em, ...: são valores exatos previamente definidos(tam minimo), mas se crescer ele vai vazar;
- 0 (zero): terá relação com a definição do flex-grow;
REVISAR: trabalha o relacionamento com outras condições de conteúdo e propriedades;
### Prática com flex-basis
um pouco mais complexo-> faça mais exercício para perceber as diferenças!

### Estrutura básica do flex-shrink
É a propriedade que estabelece a capacidade de redução ou compressão de tamanho de um item.

vimos antes flex-basis-> tamanho minimo esperado para esse item(que só expande se aumentar o conteúdo) e ainda depende do flex-grow;

aqui no flex-shrink o comportamento é inverso: set em 1 (vai permitir a redução desses itens); set em 0 (não será permitida a redução desses itens)

uma  vez que o flex-basis: 100px por exemplo não posso fazer que o item seja reduzido com o shrink o item abaixo desses 100px;

mas se eu tiver a propriedade colocada acima de 1, 2, 3; ele vai estabelecer que você vai poder reduzir 2, 3, etc relacionado ao primeiro item; haverá um cálculo no container onde vai pegar um item de tamanho base e vai utilizar para essa compressão;

seja pra crescimento (basis); ou para redução (shrink);
### Prática com flex shrink
ok revisar;
### Estrutura básica e prática com flex
Essa propriedade é um atalho ou abreviação de escrita para as propriedade: grow, shrink e basis(exatamente nessa ordem);


### Estrutura básica e prática com order
order: 0; (padrão)
order: 1;
order: 2;
order: 3;

### Estrutura básica e prática com align-self
É a propriedade que estabelece o alinhamento de modo individual sobre um item determinado. Para recebem um alinhamento diferente do padrão;
VALORES POSSÍVEL
- auto: valor padrão que irá respeitar a definição do align-items do container;
- flex-start: ao início do container;
- flex-end: ao final do container;
- center: relativo ao centro de acordo com o eixo (column, row);
- stretch: ocupar todos os espaços relativo;
- baseline: utiliza a linha base da tipografia;

## Projeto Integrador
### Apresentação e preparação do projeto
### Organizando a interface - Parte 1.1
### Organizando a interface - Parte 1.2
### Organizando a interface - Parte 1.3
### Organizando a interface - Parte 2
### Organizando a interface - Parte 3
### Conclusão do curso
### Gitlab
### Slides
### Certifique seu conhecimento