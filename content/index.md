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

Esta página descreve a proposta para o trabalho de conclusão de curso (TCC), que
será desenvolvido na disciplina MAC0499 (Trabalho de Formatura Supervisionado)
do bacharelado em Ciência da Computação no Instituto de Matemática e Estatística
da Universidade de São Paulo (IME-USP).

**Autor**: Rodrigo Orem da Silva ([email](mailto:rodrigo.orem@usp.br))  
**Supervisora**: Kelly Rosa Braghetto

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
menor conhecimento sobre o tema e influenciar a opinião
pública.<cite>[[1]](#1)</cite>

Para abordar esses problemas, propomos a construção de uma plataforma que
ofereça um ambiente mais propício para o debate público, com o apoio de
ferramentas de categorização, mediação e checagem de fatos colaborativa.

Em um trabalho anterior, foi possível implementar a versão inicial da
plataforma, disponível em <a
href="https://veredito.org">https://veredito.org</a>. As atividades desse ano
consistem no desenvolvimento de outras funcionalidades e avaliação da solução.

## Atividades

As atividades essenciais para o desenvolvimento do trabalho são:

1. **Desenvolvimento de outras funcionalidades básicas.** Além de ser possível
   discutir cada proposição com argumentos a favor e contra, será possível criar
   uma discussão livre em cada argumento. Também será possível referenciar
   fontes internas ou outros argumentos dentro dos próprios argumentos.
   
   Além disso, nessa atividade corrigiremos certos certos problemas de
   implementação que ocorrem no ambiente de produção.

1. **Categorização automática.** Ao criar uma proposição para ser debatida, o
   usuário pode atribuir _tags_, o que é útil para categorização. Será desenvolvido
   uma funcionalidade que sugere _tags_ apropriadas para a proposição do usuário
   baseada em seu texto.

1. **Detecção de argumentos duplicados.** Utilizaremos técnicas de aprendizado
   de máquina e processamento de linguagem natural para detectar argumentos
   similares, de modo a sugerir que o usuário referencie ou edite argumentos
   já existentes, caso seja apropriado.

1. **Cálculo de relevância de argumentos.** Adaptaremos o algoritmo PageRank
   para calcular a relevância dos argumentos a partir da frequência deles como
   premissa de outros argumentos. Para isso, será necessário fazer uma raspagem de
   dados na _web_ ou em alguma rede com conteúdo social, o que também é útil para
   calcular a popularidade dos argumentos.

1. **Pesquisa de usabilidade**. Será feita uma pesquisa entre usuários para
   testar a usabilidade e avaliar se o sistema é efetivo como uma plataforma de
   debates online.

1. **Redação da monografia**. Inclui, além do desenvolvimento da monografia, o
   desenvolvimento do pôster e da apresentação.

## Cronograma de atividades

O cronograma das atividades proposto é:

| Atividade                            | Abr |  Mai | Jun | Jul | Ago | Set | Out | Nov | Dez |
| ------------------------------------ | --- |  --- | --- | --- | --- | --- | --- | --- | --- |
| 1. Funcionalidades básicas           |  ✔️  |   ✔️  |  ✔️  |   ️  |   ️  |   ️  |   ️  |   ️  |   ️  |
| 2. Categorização automática          |     |      |  ✔️  | ✔️   |     |     |     |     |     |
| 3. Detecção de duplicados            |   ️  |    ️  |   ️  | ✔️   | ✔️   |     |     |     |     |
| 4. Cálculo de relevância             |   ️  |    ️  |   ️  |   ️  | ✔️   | ✔️   | ✔️   |     |     |
| 5. Pesquisa de usabilidade           |   ️  |    ️  |   ️  |   ️  |   ️  | ✔️   | ✔️   |   ️  |   ️  |
| 6. Redação da monografia             |     |      |     |     |   ️  | ✔️   | ✔️   | ✔️   | ✔️   |

## Referências

<a id="1">[1]</a>: Dan Ehrenfeld, Matt Barton, "Online Public Spheres in the
Era of Fake News: Implications for the Composition Classroom", Computers and
Composition, Volume 54, 2019, 102525, ISSN 8755-4615,
https://doi.org/10.1016/j.compcom.2019.102525.
