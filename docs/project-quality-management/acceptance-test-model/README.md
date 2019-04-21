# Modelo de Testes de Aceitação do Usuário

**Autor: Filipe Toyoshima**

20 de Abril de 2019

## Introdução

Na Engenharia, os [Testes de Aceitação do Usuário](https://en.wikipedia.org/wiki/Acceptance_testing#User_acceptance_testing) consistem em validar, junto ao usuário de determinado sistema, se a solução proposta ataca devidamente o problema que se quer resolver. Diferentemente de outros testes na área, este não consiste de um teste do sistema, para verificar ou validar seus componentes ou seu funcionamento, mas foca diretamente em como o usuário reage ao que lhe é apresentado, para que se validem as ideias que norteiam o projeto.

Este documento tem o objetivo de padronizar uma maneira de validar as ideias do projeto HubCare, no sentido de colocá-lo frente ao seu público alvo e verificar se o mesmo se enquandra com suas necessidades.

## Time de Aplicação do Teste

### Gerente de Produto

Cargo assumido por [Filipe Toyoshima](https://github.com/filipetoyoshima) no momento da escrita desse documento.

O Gerente de Produto deve, imprescindivelmente, estar presente no momento de execução dos testes, pois é de sua responsabilidade o veredito a respeito da validação da solução implementada como solução para os problemas do usuário. É, também, de sua responsabilidade a emissão de um relatório público que exponha os resultados do teste, para que toda a equipe e qualquer stakeholder tenha conhecimento dos resultados obtidos.

### Membros de EPS

Lembrando que esse projeto está sendo desenvolvido no contexto de duas disciplinas ministradas no curso de Engenharia de Software da Universidade de Brasília, alunos da disciplina de Engenharia de Produto de Software (EPS) são responsáveis pela gerência e infraestrutura do projeto.

Dito isso, é necessário que pelo menos um aluno de EPS, **além do Gerente de Produto**, esteja presente, acompanhando os resultados para que se considere, ao relatar os resultados, mais de um ponto de vista relativo às competências relacionadas aos conteúdos de EPS.

### Membros de MDS

Além de alunos de EPS, participam também do projeto alunos de Metodologia de Desenvolvimento de Software (MDS), que têm a responsabilidade de implementar o código que solucionará o problema.

Em razão do relacionamento íntimo que esses membros têm com a construção da solução, é importante que pelo menos um deles esteja presente durante a execução dos testes. Isso proporcionará um melhor entendimento sobre o problema que se quer resolver pelo time de desenvolvimento.

## Usuário de Teste

Como dito no [Documento de Visão](../../project/vision-document/README.md) o projeto tem como público-alvo as comunidades de software livre, atacando inicialmente as comunidades presentes no [GitHub](https://github.com/).

Visto isso, é necessário que o público de testes seja composto por usuários do GitHub que tenham o hábito de consumir ou contribuir para softwares livres da plataforma.

Cada pivotagem (mais detalhes no [RoadMap de Produto](../../product-roadmap/README.md)) deve contar com pelo menos 2 perfis de usuários diferentes:

- Usuário de Software Livre
- Contribuidor de Software Livre

Vale lembrar que nem toda pivotagem envolverá partes do sistema que atendam ambos os perfis indicados acima, logo, cabe ao time decidir a necessidade de ambos.

É interessante, também, que os usuários tenham características diferentes entre os testes, como por exemplo: gênero, idade, condição financeira, tempo como usuário/contribuidor de software livre, área de atuação específica, etc. Isso proporcionará uma melhor diversidade de pontos de vista nos resultados dos testes.

## Termo de Aceite

O usuário de testes deve assinar um termo com os seguintes dizeres:

> Eu, < *Inserir nome do Usuário* > , autorizo a utilização da minha imagem e som de voz, na qualidade de participante de Teste de Aceitação da Aplicação denominada HubCare, sob responsabilidade dos contribuidores do sistema a ser testado vinculado ao Programa de Graduação em Engenharia de Software da Universidade de Brasília.
>
> Minha imagem e som de voz podem ser utilizadas apenas para: análise por parte da equipe de pesquisa, apresentações em atividades acadêmicas, atividades educacionais, como por exemplo exposição em apresentações; revisão por parte dos stakeholders que desejem acesso ao insumo bruto das pesquisas para validação dos resultados gerados por análise.
>
> Tenho ciência de que não haverá divulgação da minha imagem e/ou som de voz por qualquer meio de comunicação, sejam elas televisão, rádio ou internet, exceto nas atividades vinculadas ao ensino e a pesquisa explicitadas acima. Tenho ciência também de que a guarda e demais procedimentos de segurança com relação às imagens e ao som de voz são de responsabilidade do(a) pesquisador(a) responsável.
> 
> Deste modo, declaro que autorizo, livre e espontaneamente, o uso para fins de pesquisa, nos termos acima descritos, da minha imagem e som de voz.

## Ambiente de Teste

O teste deve ocorrer num local quieto o suficiente para que o usuário não se distraia. Deve haver acomodações semelhantes às de um escritório, onde o usuários possa se sentir confortável para utilizar o sistema um computador cedido pela equipe que monitora os testes, no qual estará instalado o sistema a ser testado.

Além disso, o local deve dispor de conexão estável com a internet.

## Insumos Gerados

Devem ser gravados, durante os testes, para consultas posteriores:

- A tela do usuário
- O rosto do usuário
- A voz do usuário

Lembrando que esses dados só poderão ser coletados mediante autorização do usuário expressa no [Termo de Aceite](#Termo%20de%20Aceite).

## Script de Testes

Durante os preparativos para os testes, várias decisões acerca do que está escrito acima devem ter sido tomadas. Todas essas decisões devem ser documentas por um Script que será responsável por alinhar toda a equipe responsável. Dessa maneira, mesmo que a equipe alocada para testes tenha que ser substituída, qualquer membro poderia seguir o Script para obter os dados para análise.

O Script deve detalhar, também, passos necessários para que se gerem os dados que irão compor o Relatório de testes, descrito abaixo.

## Relatório

Seguem as informações que o relatório a ser gerado por cada sessão de testes deve conter:

### Introdução

A introdução deve explicar sobre o que o documento se trata, qual é a visão do projeto a ser testado.

Além disso, deve conter uma tabela com as seguintes informações:

- Data e horário do Teste
- Quantidade de participantes
- Versão do Software a ser testado (que coincida com a Release Note gerada no GitHub)
- Nomes dos membros presentes

### Escopo

Explicar quais as funcionalidades que serão testadas, deixando claro qual a razão de cada uma delas.

O Escopo deve ser detalhado de maneira ordinária, isto é, contendo a sequência de passos necessários para que cada funcionalidade descrita tenha sido testada.

### Metodologia

Esta seção destina-se a explicar, minuciosamente, como os testes desta sessão em particular foram realizados. Deve incluir local, quantidade de pessoas presentes, relação entre equipe de teste e usuário, como foi a interação entre os presentes e qualquer outra informação que seja relevante para replicação das condições de teste.

Devem ser descritas, também, as ferramentas utilizadas para o teste, como, por exemplo, as ferramentas usadas para gravar a tela e o áudio do usuário.

### Comentários dos Usuários

Ao final dos testes, devem ser feitas perguntas abertas sobre as impressões a respeito da aplicação testada. É necessário tomar cuidado para que as perguntas não induzam respostas, por exemplo "Você gostou dessa aplicação?" deve ser evitado, é preferível perguntar "O que você achou?". A ideia não é ter um questionário que seja respondido pelos usuários, mas sim uma conversa aberta onde o usuário possa deixar suas impressões.

### Conclusão

O relatório deve finalizar respondendo algumas perguntas e jsutificando as respostas, caso tenha sido conclusivo.

- A solução proposta resolve o problema do público-alvo?
- Existe uma maneira melhor de atacar o problema?
- O usuário de teste sentiu falta de alguma coisa?
- O usuário de teste abdicou de usar alguma parte da solução?

Caso o teste não tenha sido conclusivo, é necessário então rever a estrutura de testes, o que vai desde as decisões tomadas para uma sessão específica até as recomendações deste mesmo documento.