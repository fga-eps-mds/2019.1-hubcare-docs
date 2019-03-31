# Documento de Visão
***

## Histórico de Revisão
***

| Data | Versão | Descrição | Autor |
|:----:|:------:|:---------:|:-----:|
| 24/03/19 | 0.1 | Abertura do Documento de Visão | Brian Lui |
| 24/03/19 | 0.2 | Descrições da Parte Interessada e do Usuário | Brian Lui |
| 26/03/19 | 0.3 | Introdução | Francisco Heronildo |
| 26/03/19 | 0.4 | Recursos do Produto e Restrições | Jacó Apolinário |
| 26/03019 | 0.5 | Posicionando | Francisco Heronildo |
| 27/03/19 | 0.6 | Restrições | Jacó Apolinário |
| 27/03/19 | 0.7 | Visão Geral do Produto | Brian Lui |
| 28/03/19 | 0.8 | Revisão | Brian Lui, Francisco Heronildo, Jacó Apolinário |
 | 29/03/19 | 0.9 | Ajustes da Introdução| Francisco Heronildo, Brian Lui |
| 29/03/19 | 0.10 | Ajustes do Posicionamento | Francisco Heronildo, Brian Lui |
| 29/03/19 | 0.11 | Ajustes dos Perfis do Usuário | Francisco Heronildo, Brian Lui |
| 29/03/19 | 0.12 | Ajustes da Visão Geral do Produto | Francisco Heronildo, Brian Lui |
| 30/03/19 | 0.13 | Ajustes dos Recusos do Produto | Francisco Heronildo, Jacó |
| 30/03/19 | 0.14 | Ajustes das Restrições do Produto | Francisco Heronildo, Jacó |
| 30/03/19 | 0.15 | Faixas de Qualidade | Francisco Heronildo |
| 31/03/19 | 0.16 | Outros Requisitos do Produto | Francisco Heronildo |
| 31/03/19 | 0.16 | Índice | Francisco Heronildo |


## Índice

* [1. Introdução](#id1)
* [1.1 Propósito](#id11)
* [1.2 Escopo](#id12)
* [1.3 Definições, acrônimos e abreviações](#id13)
* [1.4 Referências](#id14)
* [1.5 Visão Geral](#id15)
* [2. Posicionando](#id2)
* [2.1 Oportunidade de Negócios](#id21)
* [2.2 Instrução do Problema](#id22)
* [2.3 Instrução de Posição do Produto](#id23)
* [3. Descrições da Parte Interessada e do Usuário](#id3)
* [3.1 Resumo dos Envolvidos](#id31)
* [3.2 Perfis dos Usuários](#id32)
* [3.2.1 Usuários do Github](#id321)
* [3.2.2 Equipe de Desenvolvedores](#id322)
* [3.3 Principais Necessidades da Parte Interessada ou do Usuário](#id33)
* [4. Visão Geral do Produto](#id4)
* [4.1 Perspectiva do Produto](#id41)
* [4.2 Resumo das Capacidades](#id4)2
* [4.3 Licenciamento e Instalação](#id43)
* [5. Recursos do Produto](#id5)
* [6. Restrições](#id6)
* [6.1 Restrições de Design](#id61)
* [6.2 Restrições Externas](#id62)
* [6.3 Restrições de Implementação](#id63)
* [7. Faixas de Qualidade](#id7)
* [8. Outros Requisitos do Produto](#id8)
* [8.1 Requisitos do Sistema](#id81)

***
## 1. Introdução
***
<div id='id1'/>

A introdução fonecerá tópicos relacionados a uma visão geral do produto, assim como próposito, escopo, definições, acrônimos, abreviações e referências do projeto.

### 1.1 Propósito
<div id='id11'/>
  
Esse documento tem como propósito, apresentar uma visão geral do desenvolvimento do hubcare, e visa auxiliar a compreensão do contexto no qual será inserido.

O hubcare é um plugin, feito para comunidade do Github, que visa verificar se os repositórios são receptives para os usuários de acordo com métricas pré-derteminadas. 

### 1.2 Escopo
<div id='id12'/>

O hubcare tem como objetivo suprir as necessidades de auxiliar os usuários do Github, na verificação de repositórios e ajuda-ló a fazer escolhas atráves de dados, seja um contribuidor que quer saber se a contribuçao vai ser aceita pela comunidade ou um usuário do software que quer saber se ele terá suporte ou será abandonado pela comunidade, assim, zelando a qualidade da mesma.

### 1.3 Definições, acrônimos e abreviações
<div id='id13'/>

* Hubcare - Nome do Plug-in
* UnB - Universidade de Brasília
* MDS - Métodos de Desenvolvimento de Software
* EPS - Engenharia de Protudo de Software
* PR's - Pull Requests

### 1.4 Referências
<div id='id14'/>

* [**IBM Knowledge Center.**](https://www.ibm.com/support/knowledgecenter/pt-br/SSYMRC_6.0.5/com.ibm.rational.rrm.help.doc/topics/r_vision_doc.html) Acessado em 24 de Março de 2019.

### 1.5 Visão geral
<div id='id15'/>

O documento de visão descreve os características e utilidades da aplicação. São apresentados o problema que motivou o desenvolvimento do software, o posicionamento do produto, descrição da parte interessada e do usuário, recursos, restrições e requisitos do produto.


***
## 2. Posicionando
*** 
<div id='id2'/>

### 2.1 Oportunidade de Negócios
<div id='id21'/>

O hubcare é direcionado para os usuários, que terá conhecimento do nível de receptividade dos seus repositórios, também para contribuidores, que pretendem fazer uma contribuição para algum projeto. 

Atualmente para contribuir com projetos no Github é simples , porém, exite um problema, o usuário não tem a certeza se irá ter um retorno sobre aquele projeto. Desse modo, o hubcare será desenvolvido para fazer essas verificações e classificar se o repositório é ideal.

### 2.2 Instrução do Problema
<div id='id22'/>

| Tipo | Descrição |
|:----:|:---------:|
|**Problema**| Contribuir para um repositório que seja pouco receptivo |
|**Afeta**| Contribuidores do Github |
|**Impactos**| Contribuidor gastará tempo em um projeto não muito ativo |
|**Solução**| apresentará dados da saúde do repositório |

<br><br/>

| Tipo | Descrição |
|:----:|:---------:|
|**Problema**| O usuário não tem conhecimento se o seu repositório é atrativo para comunidade |
|**Afeta**| Usuários do Github |
|**Impactos**| O usuário não terá ajuda da comunidade em seu projeto |
|**Solução**| apresentará dados da saúde do repositório |

### 2.3 Instrução de Posição do Produto 
<div id='id23'/>

| Tipo | Descrição |
|:----:|:---------:|
|**Público Alvo**| Comunidade do Github |
|**Carências**| Exibição intuitiva dos dados do repositório |
|**Solução**| Hubcare |
|**Solução Descrição da Solução**| Plugin que apresentará dados a respeito do repositório de forma intuitiva |
|**Diferenciais**| Primeiro software a realizar essa aplicação |

***
## 3. Descrições da Parte Interessada e do Usuário
***
<div id='id3'/>

### 3.1 Resumo dos Envolvidos
<div id='id31'/>

| Nome | Descrição | Responsabilidades |
|:----:|:---------:|:-----------------:|
| Usuários do Github | Pessoas que utilizam a plataforma, Github. | Avaliar a qualidade deste sistema para que os usuários da plataforma se beneficiem cada vez mais.
| Equipe de desenvolvimento do projeto | A Equipe é composta por alunos de graduação do Curso de Engenharia de Software da Universidade de Brasília, discentes na matéria Métodos de Desenvolvimento de Software ou Engenharia de Produto de Software. | Planejar, desenvolver, testar, documentar e implementar o sistema. |

### 3.2 Perfis dos Usuários
<div id='id32'/>

#### 3.2.1	Usuários do Github
<div id='id321'/>

<table>
  <tr><th>Descrição</th><td>Contribuidores e usuários de projeto do Github com o interesse em medir a receptividade de um determinado repositório.</td></tr>
  <tr><th>Tipo</th><td>Conhecimento da plataforma do Github.</td></tr>
  <tr><th>Responsabilidades</th><td> Testar o plugin e dar o feedback se o repositório é mesmo receptível de acordo com os dados demonstrados.</td></tr>
  <tr><th>Critérios de Sucesso </th><td>O repositório escolhido pelo usuário apresentar a receptividade de acordo com os resultados apresentado no Plugin.</td></tr>
  <tr><th> Envolvimento </th><td> Alto </td></tr>
  <tr><th> Comentários / Problemas </th><td> - </td></tr>
</table>

#### 3.2.2	Equipe de Desenvolvedores
<div id='id322'/>

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

### 3.3 Principais Necessidades da Parte Interessada ou do Usuário
<div id='id33'/>

| Necessidade | Prioridade | Preocupações | Solução Atual | Soluções Propostas |
|:---:|:---:|:---:|:---:|:---:|
| Dados com as métricas que irão medir o nível de receptividade dos repositórios e se o mesmo está ativo , dando suporte ao usuário. | Alta | Falta de métricas e de confiança dessas métricas. | Verificação manual das métricas dos repositórios. | Realizar a leitura dos dados da API do github, com isso será criado métricas, e assim gerando indicadores de um determinado repositório, para assim mostrar o nível de saúde. |

***
## 4. Visão Geral do Produto
***
<div id='id4'/>

### 4.1 Perspectiva do Produto
<div id='id41'/>

O Hubcare irá automatizar o processo de análise de um determinado repositório que seja de interesse do usuário, mostrando se o  mesmo está ativo e se é receptível. O plugin fornecerá dados de acordo com métricas pré-determinadas, para os usuários com os dados necessários para saber o nível de receptividade. Deste modo, é possível agilizar o processo em que um usuário tenha que entrar em um repositório e analisar todas essas métricas um por um. 

### 4.2 Resumo das Capacidades
<div id='id42'/>

<table>

  <tr><th>Benefício para o Cliente</th><th>Recursos de Suporte</td></tr>
  <tr><td>Agilidade na análise dos dados de algum repositório.</th><td>Será apresentada uma base de dados, em que o usuário poderá identificar rapidamente a saúde do repositório..</td></tr>
  
</table>

### 4.3 Licenciamento e Instalação
<div id='id43'/>

Será necessário a instalação do plugin que estará disponível na Chrome Store do navegador Google Chrome. O licenciamento do produto será do tipo MIT(software livre). Ou seja, qualquer pessoa que adquirir uma cópia dos arquivos deste software, poderá lidar com ele sem restrições e sem limitação do direito de uso, cópia, publicação, publicar ou até mesmo vender.

***
## 5. Recursos do Produto 
***
<div id='id5'/>

O Hubcare através de dados coletados da API do Github,deve ser um plugin capaz de fornecer informações sobre os repositórios,verificando se ele é ativo,receptivo,e se fornece assistência à comunidade do Github.

***
## 6. Restrições
***
<div id='id6'/>

### 6.1 Restrições de Design
<div id='id61'/>

O plugin deve ter uma interface que seja de fácil compreensão, para a comunidade do Github, de forma que seja de facil compreensão.

### 6.2 Retrições Externas
<div id='id62'/>

Pequenos impasses na equipe de desenvolvimento e inexperiência na linguagem e Framework da aplicação.

### 6.3 Restrições de Implementação
<div id='id63'/>

O software deverá ser desenvolvido nas linguagens HTML/CSS,JavaScript e Python com a utilização do Framework Django para aplicação web.

***
## 7. Faixas de Qualidade
***
<div id='id7'/>

O plugin será disponibilizado na Chrome Web Store para maior eficiência em dispositivos que tenham suporte com o navegador Google Chrome e conexão com a internet.


***
## 8. Outros Requisitos do Produto
***
<div id='id8'/>

### 8.1 Requisitos do Sistema
<div id='id81'/>

   Dispositivo que tenham suporte com o Navegador Google Chrome e acesso a internet