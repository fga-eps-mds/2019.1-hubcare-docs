# Documento de visão
***

## Histórico de Revisão
***

| Data | Versão | Descrição | Autor |
|:----:|:------:|:---------:|:-----:|
| 24/03/19 | 0.1 | Abertura do Documento de Visão | Brian Lui |
| 24/03/19 | 0.2 | Descrições dos Envolvidos e dos Usuários | Brian Lui |
| 26/03/19 | 0.3 | Introdução | Francisco Heronildo |
| 26/03/19 | 0.4 | Recursos do Produto e Restrições | Jacó Apolinário |
| 26/03019 | 0.5 | Posicionando | Francisco Heronildo |
| 27/03/19 | 0.6 | Restrições | Jacó Apolinário |
| 27/03/19 | 0.7 | Visão Geral do Produto | Brian Lui |
 
***
## 1. Introdução
***

Esta introdução fonecerá tópicos relacionados a uma visão geral do produto, assim como próposito, escopo, definições, acrônimos, abreviações e referências do projeto.

### 1.1 Propósito
  
Esse documento tem como propósito, apresentar uma visão geral do desenvolvimento do hubcare, e visa auxiliar a compreensão do contexto no qual será inserido.

### 1.2 Escopo

O hubcare tem como objetivo suprir as necessidades de auxiliar os usuários do Github, na verificação de repositórios ativo, receptivos e que lhe darão surporte, assim, zelando a qualidade da comunidade.

### 1.3 Definições, acrônimos e abreviações

* Hubcare - Nome do Plug-in
* UnB - Universidade de Brasília
* MDS - Métodos de Desenvolvimento de Software
* EPS - Engenharia de Protudo de Software

### 1.4 Referências

* [**IBM Knowledge Center.**](https://www.ibm.com/support/knowledgecenter/pt-br/SSYMRC_6.0.5/com.ibm.rational.rrm.help.doc/topics/r_vision_doc.html) Acessado em 24 de Março de 2019.

### 1.5 Visão geral

O documento de visão descreve os detalhes sobre as características e utilidades do plugin a ser desenvolvido. São apresentados o problema que motivou o desenvolvimento do software, o posicionamento do produto, descrição da parte interessada e do usuário, recursos, restrições e requisitos do produto.


***
## 2. Posicionando
*** 

### 2.1 Oportunidade de Negócios

Atualmente para contribuir com projetos no Github é simples , porém, exite um problema, o usuário não tem a certeza se irá ter um retorno sobre aquele projeto.

Hubcare, será desevolvido para fazer essa verificação nos repositórios da comunidade e classifica-ló se é ideal para contribuição.  

### 2.2 Instrução do Problema

O problema de verificar a saúde do repositório afeta usuários do Github que tenham contribuido com algum repositório inativo, não receptivo ou sem suporte. O impacto do problema é que o contribuidor gastará tempo em um projeto inativo. Uma solução bem sucedida incluiria desenvolvimendo de um software verificação para auxilar a comunidade.

### 2.3 	Instrução de Posição do Produto 

Para os usuários da comunidade do Github que gostam contribuir com alguns projetos. O Hubcare é um plug-in que verificar a saúde do repositório. De outro modo sem concorrentes no momento, nosso produto preza pela qualidade dos repositórios do Github.

***
## 3. Descrições dos Envolvidos e dos Usuários
***

### 3.1 Resumo dos Envolvidos
| Nome | Descrição | Responsabilidades |
|:----:|:---------:|:-----------------:|
| Investidores | Usuários do Github. | Avaliar a qualidade deste sistema para que os usuários da plataforma se beneficiem cada vez mais.
| Equipe de desenvolvimento do projeto | A Equipe é composta por alunos de graduação do Curso de Engenharia de Software da Universidade de Brasília, discentes na matéria Métodos de Desenvolvimento de Software ou Engenharia de Produto de Software. | Planejar, desenvolver, testar, documentar e implementar o sistema. |

### 3.2 Perfis dos Usuários

#### 3.2.1	Investidores
<table>
  <tr><th>Descrição</th><td>Usuários do Github com o interesse em medir a receptividade de um determinado repositório.</td></tr>
  <tr><th>Tipo</th><td>Conhecimento da plataforma do Github.</td></tr>
  <tr><th>Responsabilidades</th><td> Testar o plugin e dar o feedback se o repositório é mesmo receptível de acordo com os dados demonstrados.</td></tr>
  <tr><th>Critérios de Sucesso </th><td>O repositório escolhido pelo usuário apresentar a receptividade de acordo com os resultados apresentado no Plugin.</td></tr>
  <tr><th> Envolvimento </th><td> Alto </td></tr>
  <tr><th> Comentários / Problemas </th><td> - </td></tr>
</table>

#### 3.2.2	Equipe de Desenvolvedores
<table>
  <tr><th> Representantes </th><td>
  Cleber José de Castro Júnior<br>
  Lucas Hiroshi Horinouchi<br>
  Filipe Toyoshima Silva<br>
  Rômulo Vínicius de Souza<br>
  Brian Lui<br>
  Francisco Heronildo Sousa Santos<br>
  Vitor Meireles Oliveira<br>
  Jacó Apolinário da Silva<br>
  João Vitor Ferreira Alves<br></td></tr>
  <tr><th>Descrição</th><td>Desenvolvedores do projeto</td></tr>
  <tr><th>Tipo</th><td> A Equipe é composta por alunos de graduação do Curso de Engenharia de Software da Universidade de Brasília, no Campus do Gama, 5 discentes na matéria Métodos de Desenvolvimento de Software 4 discentes em Engenharia de Produto de Software.</td></tr>
  <tr><th>Responsabilidades</th><td>Planejar o projeto, programar os recursos definidos do projeto, realizar testes de implementação, documentar a estrutura do software e implementar o sistema de acordo com a documentação.</td></tr>
  <tr><th>Critérios de Sucesso</th><td>O Plugin ser aceito pela comunidade do Github e ser bastante utilizada pelos usuários.</td></tr>
  <tr><th>Envolvimento</th><td>Alto</td></tr>
  <tr><th>Comentários / Problemas</th><td>-</td></tr>
</table>

### 3.3 Principais Necessidades dos Usuários ou dos Envolvidos

| Necessidade | Prioridade | Preocupações | Solução Atual | Soluções Propostas |
|:---:|:---:|:---:|:---:|:---:|
| Dados com as métricas que irão medir o nível de receptividade dos repositórios do Github. | Alta | Falta de métricas e de confiança dessas métricas. | Verificação manual das métricas dos repositórios. | Realizar a leitura dessas métricas, juntar todos em um plugin , e deste modo gerar dados que irão mostar o nível de saúde dos repositórios. |

***
## 4. Visão Geral do Produto
***

### 4.1 Perspectiva do Produto

O Hubcare irá automatizar o processo de análise de um determinado repositório que seja de interesse do usuário, mostrando se o  mesmo está ativo e se é receptível. O plugin fornecerá dados de acordo com métricas pré-determinadas, para os usuários com os dados necessários para saber o nível de receptividade. Tais métricas contemplam pull requests aceitos e rejeitados, número de issues abertas, fechadas, com comentários e sem comentários,número de commits. Deste modo, é possível agilizar o processo em que um usuário tenha que entrar em um repositório e analisar todas essas métricas um por um. 

### 4.2 Resumo das Capacidades

<table>

  <tr><th>Benefício para o Cliente</th><th>Recursos de Suporte</td></tr>
  <tr><td>Agilidade na análise dos dados de algum repositório.</th><td>Será apresentada uma base de dados, em que o usuário poderá identificar rapidamente a saúde do repositório..</td></tr>
  
</table>

### 4.3 Licenciamento e Instalação

Será a instalação do plugin no Chrome. O licenciamento do produto será do tipo MIT(software livre). Ou seja, qualquer pessoa que adquirir uma cópia dos arquivos deste software, poderá lidar com ele sem restrições e sem limitação do direito de uso, cópia, publicação, publicar ou até mesmo vender.

***
## 5. Recursos do Produto 
***

### 5.1 Verificar se o repositorio está ativo
  O usuário poderá verificar se o repositório está ativo, de acordo com quantidade de commits no ultimo mês e sua qualidade de aceitação de PRs.

### 5.2 Verificar a receptividade para novos colaboradores
  Verificar se o repositório é receptivo através da qualidade de aceitação de PRs e a quantidade de contribuidores diferentes no ultimo mês, levando em conta também a taxas de issues ativas e se possui Realease notes, Template de Pull Request e uma Taxa de Good-First-Issues.

### 5.3 Verificação de Suporte
  Analisar se o repositório possui suporte ao usuário, com a verificação de ReadMe, Template de issues, se o repositório possui Licença,Código de Conduta e se possui alguma descrição com informações para o usuário que queira contribuir. 
  
***
## 6. Restrições
***
* É necessário conexão com Internet.
* É necessário API do Github.
* Só poderá ser usado no Chrome.