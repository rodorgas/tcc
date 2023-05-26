---
title: "Proposta de TCC: Plataforma de Debates"
menu:
  main:
    name: Home
    weight: -100
    url: /
    params:
      icon: home
---

Esta página descreve a proposta para o trabalho de conclusão de curso (TCC),
que será desenvolvido na disciplina MAC0499 (Trabalho de Formatura
Supervisionado) do bacharelado em Ciência da Computação no Instituto de
Matemática e Estatística da Universidade de São Paulo (IME-USP).

**Autor**: Rodrigo Orem da Silva ([email](mailto:rodrigo.orem@usp.br))  
**Supervisora**: Kelly Rosa Braghetto

## Motivação

A esfera pública é um espaço fundamental na democracia onde as pessoas podem se
reunir para discutir livremente e identificar os problemas da sociedade. As
plataformas sociais são meios de comunicação importantes para o exercício da
cidadania e o público que produz e consome as informações nessas plataformas
facilita a criação de uma esfera pública digital crítica e racional que pode
apoiar o debate público, a deliberação e formação de comunidades, além de
melhorar a participação dos cidadãos na tomada de decisões políticas
<a href="#Ehrenfeld-e-Barton-2019" id="Ehrenfeld-e-Barton-2019-1">(Ehrenfeld e Barton, 2019)</a>
<a href="#Snellen-et-al-2012" id="Snellen-et-al-2012-1">(Snellen et al., 2012)</a>
.

Atualmente, o debate nas redes sociais ocorre por meio de postagens, de
repostagens (em que um usuário republica certo conteúdo com seu próprio
comentário), e de seções de comentários. Geralmente, os comentários mais
populares (que receberam mais curtidas ou mais respostas) são exibidos
primeiro. Os sites de notícias e agregadores de *links* sociais também possuem
seções de comentários que permitem que os leitores comentem e escrevam réplicas
aos outros comentários, geralmente em uma estrutura de árvore. Já os fóruns de
discussão costumam exibir as mensagens de maneira cronológica e para responder
a uma mensagem específica, ela é reproduzida na resposta.

No entanto, essas plataformas possuem diversos problemas, como as bolhas
ideológicas, que reforçam crenças pessoais e excluem opiniões opostas
<a href="#Mounk-2018" id="Mounk-2018-1">(Mounk, 2018)</a>
. Além disso, foi observado distorção da
informação, ataques pessoais, propagação de desinformação e prejuízo à
reputação da plataforma
<a href="#Diakopoulos-e-Naaman-2011" id="Diakopoulos-e-Naaman-2011-1">(Diakopoulos e Naaman, 2011)</a>.

Para abordar esses problemas, um trabalho propôs o Kialo, uma plataforma de
debate estruturado que foi projetada para repensar o papel do debate em
pesquisa, divulgação científica e ensino, principalmente na área de ciência
política. Essa plataforma divide os argumentos de cada tema de discussão entre
prós e contras, e o debate é exibido visualmente com uma estrutura de árvore
<a href="#Chaudoin-et-al-2017" id="Chaudoin-et-al-2017-1">(Chaudoin et al., 2017)</a>.

Atualmente o Kialo possui quase 18 mil debates e mais de 700 mil argumentos, de
modo a ser a principal ferramenta de argumentação colaborativa publicamente
disponível. Acreditamos que, embora uma visualização em árvore da discussão
seja intuitiva, ela pode dificultar a compreensão já que o conteúdo fica
fragmentado e são necessárias várias interações com a aplicação para ler um
argumento com profundidade. Além disso, o contexto de uma discussão pode ser
perdido ao navegar na árvore, de modo que subargumentos mais profundos podem
não ser aplicáveis à discussão original.

Outro trabalho desenvolveu o Spirited, uma ferramenta de debate estruturado em
que a discussão é feita ao redor de um artigo de opinião. Os argumentos são
construídos na forma de anotações no artigo e os usuários podem votar nas
anotações e nas sentenças do artigo. Os autores acreditam que manter uma
estrutura menos rigorosa e mais livre favorece o engajamento e gera discussões
mais interessantes 
<a href="#Mcelfresh-2016" id="Mcelfresh-2016-1">(Mcelfresh, 2016)</a>.

Observa-se, no entanto, que plataformas de anotações colaborativas enfrentam
problemas de engajamento, de modo que o único caso de sucesso é o Genius,
voltado à interpretação de significados das letras das músicas
<a href="#Mcelfresh-2016" id="Mcelfresh-2016-2">(Mcelfresh, 2016)</a>.
Além disso, com essa estrutura de debates mais flexível, é mais difícil
organizar, classificar e reusar partes da discussão.

## Objetivos

Para abordar esses problemas, propõe-se a construção do Veredito, uma
plataforma que pretende oferecer um ambiente mais propício para o debate
público com o apoio de ferramentas de categorização, mediação e checagem de
fatos colaborativa.

Nessa ferramenta, as discussões são organizadas em tópicos com argumentos
divididos entre prós e contras. É possível rebater cada argumento com
contra-argumentos em apenas um nível de discussão, limitação que pretende
evitar os problemas da estrutura em árvore. Não é possível acrescentar
subargumentos a favor: caso o usuário acredite que é possível complementar um
argumento com dados ou outro raciocínio, é possível sugerir uma edição no
próprio texto. Nesse formato é possível ter argumentos mais autocontidos, o que
pode facilitar a leitura e compreensão do assunto.

Caso um ponto da discussão seja mais polêmico, é possível criar um novo tópico
e referenciá-lo no argumento, de modo a usá-lo como hipótese. Assim, a
comunidade pode ter discussões paralelas de assuntos tangenciais em contextos
separados, sem que a plataforma perca a relação semântica entre esses assuntos.

Pretende-se também aplicar tecnologias de aprendizado de máquina e
processamento de linguagem natural para facilitar as atividades de moderação.
Além disso, serão usadas técnicas de raspagem de dados e inteligência
artificial para fornecer aos usuários informações sobre a relevância e
popularidade de um argumento.

Em um trabalho anterior, foi possível implementar a versão inicial da
plataforma (disponível em
<a href="https://veredito.org">https://veredito.org/</a>
). Agora, para a
continuidade do projeto, as atividades consistem no desenvolvimento de outras
funcionalidades e na avaliação da solução.

## Metodologia

Atualmente, a plataforma é composta por dois componentes: o *frontend* (uma
interface gráfica web), e o *backend* (o servidor responsável por coordenar as
operações e gerir os dados da aplicação). O projeto é principalmente escrito em
TypeScript, uma linguagem de programação fortemente tipada que transpila para
JavaScript.

### *Frontend*

A interface gráfica do Veredito ([figura 1](#figura-1)) é web e responsiva, de
modo a funcionar tanto em *desktops* quanto em dispositivos móveis. Ela usa
React, uma biblioteca que facilita o desenvolvimento de aplicações web
interativas, e Tailwind, um arcabouço de CSS que facilita o uso de um sistema
de design coerente em toda a interface. 

<div id="figura-1">
{{< figure src="topico.png" title="Figura 1: Discussão de um tópico no Veredito." >}}
</div>

### *Backend*

Os dados na plataforma são representados de acordo com o modelo de dados
relacional. O esquema do banco de dados relacional da plataforma é mostrado na
[figura 2](#figura-2). Na implementação foi utilizado o sistema
gerenciador de banco de dados PostgreSQL.

<div style="max-width: 25em; text-align: center; margin: auto;" id="figura-2">
{{< figure src="diagrama-modelo.png" title="Figura 2: Diagrama do modelo de dados do Veredito." >}}
</div>

A interação na plataforma é dada por meio de tópicos, que podem conter
argumentos prós ou contras. Como há muitas relações e atributos em comum entre
tópicos e argumentos, os dois são representados pela mesma entidade
*proposition*. É possível diferenciá-los pelo atributo *topic_id*, afinal,
argumentos referenciam a *proposition* correspondente ao tópico que eles
pertencem, enquanto tópicos têm esse campo em branco.

Todas as edições são armazenadas em *proposition_history*, de modo a permitir o
desfazimento de uma edição que piorou ou vandalizou o conteúdo. Quando o
usuário está registrado, seu nome de usuário é associado à edição, caso
contrário, o endereço de IP também é salvo.

Para manipular esses dados, existe um serviço em Node.js que disponibiliza uma
API que usa a linguagem de consulta GraphQL. Esse serviço usa o arcabouço
NestJS, que facilita o uso de padrões arquiteturais e o desenvolvimento de
aplicações testáveis, escalonáveis e frouxamente acopladas. Esse serviço é
dividido nos seguintes módulos:

- *user*: permite cadastrar um novo usuário, autenticar um usuário, encerrar a
sessão e obter informações sobre os usuários;

- *topic*: permite consultar tópicos de debate e criar um novo tópico;

- *argument*: permite criar, editar e listar argumentos, além de listar o histórico
de revisões do argumento; vote: permite votar em uma proposição ou remover o
voto.

- *vote*: permite votar em uma proposição ou remover o voto.

## Atividades

As atividades essenciais para o desenvolvimento do trabalho são:

1. **Desenvolvimento de outras funcionalidades básicas**. Além de ser possível
   discutir cada proposição com argumentos a favor e contra, será possível
   criar uma discussão livre em cada argumento. Também será possível
   referenciar fontes internas ou outros argumentos dentro dos próprios
   argumentos.

   Além disso, nessa atividade corrigiremos certos problemas que estão
   ocorrendo no ambiente de produção da implementação atual.

1. **Categorização automática**. Ao criar uma proposição para ser debatida, o
   usuário pode atribuir *tags*, o que é útil para categorização. Será
   desenvolvida uma funcionalidade que sugere *tags* apropriadas para a
   proposição do usuário baseadas em seu texto.

1. **Detecção de argumentos duplicados**. Utilizaremos técnicas de aprendizado
   de máquina e processamento de linguagem natural para detectar argumentos
   similares, de modo a sugerir que o usuário referencie ou edite argumentos já
   existentes, caso seja apropriado.

1. **Cálculo de relevância de argumentos**. Adaptaremos o algoritmo PageRank
   para calcular a relevância dos argumentos a partir da frequência deles como
   premissa de outros argumentos. Para isso, será necessário fazer uma raspagem
   de dados na web ou em alguma rede com conteúdo social, o que também é útil
   para calcular a popularidade dos argumentos.

1. **Avaliação de usabilidade**. Será feita uma pesquisa entre usuários para
   avaliar a usabilidade e efetividade como uma plataforma de debates online.

1. **Redação da monografia**. Inclui, além do desenvolvimento da monografia, o
   desenvolvimento do pôster e da apresentação.

## Cronograma de atividades

O cronograma das atividades proposto é:

| Atividade                            | Abr |  Mai | Jun | Jul | Ago | Set | Out | Nov | Dez |
| ------------------------------------ | --- |  --- | --- | --- | --- | --- | --- | --- | --- |
| 1. Funcionalidades básicas           |  ✔️  |   ✔️  |  ✔️  |   ️  |   ️  |   ️  |   ️  |   ️  |   ️  |
| 2. Categorização automática         |     |      |  ✔️  | ✔️   |     |     |     |     |     |
| 3. Detecção de duplicados            |   ️  |    ️  |   ️  | ✔️   | ✔️   |     |     |     |     |
| 4. Cálculo de relevância             |   ️  |    ️  |   ️  |   ️  | ✔️   | ✔️   | ✔️   |     |     |
| 5. Pesquisa de usabilidade           |   ️  |    ️  |   ️  |   ️  |   ️  | ✔️   | ✔️   |   ️  |   ️  |
| 6. Redação da monografia             |     |      |     |     |   ️  | ✔️   | ✔️   | ✔️   | ✔️   |

## Referências

1. ^
<sup>
  <a href="#Ehrenfeld-e-Barton-2019-1">[a]</a>
</sup>
<span id="Ehrenfeld-e-Barton-2019">[Ehrenfeld e Barton, 2019]</span> Dan
Ehrenfeld, Matt Barton, “Online Public Spheres in the Era of Fake News:
Implications for the Composition Classroom”, Computers and Composition, Volume
54, 2019, 102525, ISSN 8755-4615.

1. ^
<sup>
  <a href="#Snellen-et-al-2012-1">[a]</a>
</sup>
<span id="Snellen-et-al-2012">[Snellen et al. 2012]</span>
I Th M Snellen, Marcel Thaens e Wim BHJ van de Donk. Public administration in
the information age: Revisited. Vol. 19. IOS press, 2012, pp. 53, 54 (citado na
pg. 1).

1. ^
<sup>
  <a href="#Mounk-2018-1">[a]</a>
</sup>
<span id="Mounk-2018">[Mounk 2018]</span>
Yascha Mounk. “The people vs. democracy”. In: The People vs. Demo-
cracy. Harvard University Press, 2018 (citado na pg. 1).

1. ^
<sup>
  <a href="#Diakopoulos-e-Naaman-2011-1">[a]</a>
</sup>
<span id="Diakopoulos-e-Naaman-2011">[Diakopoulos e Naaman 2011]</span>
Nicholas Diakopoulos e Mor Naaman. “Towards quality discourse in online news
comments”. In: Proceedings of the ACM 2011 conference on Computer supported
cooperative work. 2011, pp. 133–142 (citado na pg. 1).

1. ^
<sup>
  <a href="#Chaudoin-et-al-2017-1">[a]</a>
</sup>
<span id="Chaudoin-et-al-2017">[Chaudoin et al., 2017]</span>
Stephen Chaudoin, Jacob Shapiro e Dustin Tingley.
“Revolutionizing teaching and research with a structured debate platform”.
Journal of Political Science 58 (2017), pp. 1064–1082 (citado na pg. 2).

1. ^
<sup>
  <a href="#Mcelfresh-2016-1">[a]</a>
  <a href="#Mcelfresh-2016-2">[b]</a>
</sup>
<span id="Mcelfresh-2016">[Mcelfresh, 2016]</span>
Joshua Mcelfresh. Spirited: A Web Application for Structured Debate. Harvard
University, 2016 (citado na pg. 3).
