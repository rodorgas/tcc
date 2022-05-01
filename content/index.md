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

Vamos apresentar nossa proposta de trabalho de conclusão de curso (TCC), que
será desenvolvido na disciplina MAC0499 (Trabalho de Formatura Supervisionado)
do bacharelado em Ciência da Computação no Instituto de Matemática e
Estatística da Universidade de São Paulo (IME-USP).

**Autor**: Rodrigo Orem da Silva ([email](mailto:rodrigo.orem@usp.br))  
**Supervisores**: Alfredo G. Vel Lejbman, Andre I. Leirner

## Motivação

A esfera pública é um espaço fundamental na democracia, onde as pessoas podem
se reunir para discutir livremente e identificar os problemas da sociedade e,
por meio dessa discussão, influenciar a ação política. Boa parte dessa
discussão acontece virtualmente nas redes sociais, onde há poucos mecanismos de
organização ou mediação, o que gera debates de baixa qualidade.

Entre os problemas identificados no debate público online estão a falta de
acesso a dados sobre o tema, falta de conhecimento dos argumentos contrários e
prevalência de ataques pessoais. Além disso, há também o uso de informações
falsas ou enganosas para sustentar argumentos, de modo a manipular pessoas com
menor conhecimento sobre o tema e influenciar a opinião pública.<cite>[[1]](#1)</cite>

Para abordar esses problemas, propomos a construção de uma plataforma que
ofereça um ambiente mais propício para o debate público, com o apoio de
ferramentas de categorização, mediação e checagem de fatos colaborativa.

## Atividades
As atividades essenciais para o desenvolvimento do trabalho são:

0. **Estudo sobre o domínio do problema**. Problemas envolvendo a opinião
   pública são abordados pela teoria da escolha social, uma estrutura teórica
   que agrega insumos individuais (como opiniões, preferências e interesses
   individuais) em resultados coletivos (como decisões, preferências e
   julgamentos coletivos).<cite>[[2]](#2)</cite> Conhecer essa área de estudo
   será fundamental para propor um sistema efetivo.

1. **Definição da arquitetura do sistema**. Nessa etapa, vamos definir as
   entidades fundamentais do sistema e como elas se relacionam entre si.
   Algumas perguntas que serão respondidas nessa etapa incluem: Como as
   opiniões são organizadas numa discussão? Como funcionará o sistema de
   votação? Os argumentos poderão ser editados, incluindo por outras pessoas?
   Como funcionará o sistema de mediação?

2. **Desenho das interfaces de usuário**. O desenho de protótipos será muito
   útil no começo do desenvolvimento, tanto para concretizar as ideias sobre o
   funcionamento da aplicação quanto para mapear a jornada do usuário, que
   orientará a implementação do sistema.

3. **Modelagem do banco de dados**. Projetaremos um modelo para os
   dados e o implementaremos em um sistema gerenciador de banco de dados.

4. **Implementação do sistema**. Essa etapa abrange todas as tarefas
   relacionadas a codificação do *frontend* e do *backend* e o provisionamento
   da aplicação. Além disso, esse sistema será integrado, como plugin de
   debates, a outro sistema existente de deliberação coletiva.

5. **Coleta de *feedback* e análise de uso**. Após a implementação, teremos
   dados reais de uso da aplicação. Esses dados podem ser usados para validar a
   efetividade da implementação e servir de insumo para outra iteração de
   desenvolvimento.

6. **Redação da monografia**. Inclui, além do desenvolvimento da monografia, o
   desenvolvimento do pôster e da apresentação.


## Cronograma de atividades

Propomos o seguinte cronograma para as atividades desenvolvidas nesse TCC:

| Atividade                             | Mar | Abr | Mai | Jun | Jul | Ago | Set | Out | Nov | Dez |
| ------------------------------------  | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Estudo sobre o domínio do problema    |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |
| Definição da arquitetura do sistema   |     |  ✔️  |  ✔️  |  ✔️  |     |     |     |     |     |     |
| Desenho das interfaces de usuário     |     |  ✔️  |  ✔️  |  ✔️  |     |     |     |     |     |     |
| Modelagem do banco de dados           |     |     |  ✔️  |  ✔️  |  ✔️  |     |     |     |     |     |
| Implementação do sistema              |     |     |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |
| Coleta de *feedback* e análise de uso |     |     |     |     |     |     |  ✔️  |  ✔️  |  ✔️  |  ✔️  |
| Redação da monografia                 |     |     |     |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |  ✔️  |

## Referências
<a id="1">[1]</a>: Dan Ehrenfeld, Matt Barton, "Online Public Spheres in the
Era of Fake News: Implications for the Composition Classroom", Computers and
Composition, Volume 54, 2019, 102525, ISSN 8755-4615,
https://doi.org/10.1016/j.compcom.2019.102525.

<a id="2">[2]</a>: List, Christian, "Social Choice Theory", The Stanford
Encyclopedia of Philosophy (Spring 2022 Edition), Edward N. Zalta (ed.),
https://plato.stanford.edu/archives/spr2022/entries/social-choice/
