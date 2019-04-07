# Plano de Gerenciamento do Projeto

**Autor: Lucas Hiroshi Horinouchi**

## Ciclo de Vida do Projeto
<br>


## Diretrizes para a execução do Projeto
<br>

## Plano de Gerenciamento de Mudanças
<br>

## Plano de Gerenciamento de Configuração de Software

Esta seção define as ferramentas e as politicas a serem seguidas durante o projeto.

### Ferramentas
####  Code
IDE adotada como padrão pela equipe devido a sua facilidade de uso.

#### Coverage
Ferramenta de execução de switch de teste que foi definida como padrão para o projeto.

#### Coveralls
Ferramenta para geração de relatórios de testes.
 
#### Django
Este foi o Framework adotado pela equipe ele sendo ele em Python.

#### Git
O Git é utilizado para o versionamento do código.

#### GitHub
Uma plataforma que permite a hospedagem de repositórios, controle de versão, marcação de atividades para os membros de time e documentação do projeto.


### Políticas

#### Política de Commits

Os commits devem ser significativos e feitos de forma sucinta descrevendo o que foi feito, portanto o commit deve ser atômico descrevendo a funcionalidade que foi implementada.

E caso exista necessidade comentar com mais detalhes o que foi implementado e o motivo.

Exemplo - "Create new class for user"


### Política de Branches

O repositório do projeto possui duas branches principais para o desenvolvimento: master e devel, e as branches auxiliares contendo as funcionalidades desenvolvidas.

A branch master conterá a versão estável, o seu conteúdo será proveniente da branch de desenvolvimento (devel) após a aprovação do pull request. 

A branch devel será utilizada para o desenvolvimento, onde a integração das funcionalidades desenvolvidas pela equipe nas branches auxiliares ocorrerá.

As branches auxiliares serão utilizadas para o desenvolvimento das funcionalidades.Essas branches serão nomeadas de acordo com a issue qual ela é relacionada.

* Exemplo : "feature-create_new_user".

Os bugs seguirão o formato padrão no projeto: bug-< Nome do bug> e dentro dele uma descrição do problema e se necessário o fluxo que levou até o bug.

* Exemplo : "bug-login".

### Política de Aprovação do Código

O nome do __pull request__ será o nome da issue sendo feito de sua branch para a devel.

O __PO__ é o responsavel de avaliar os __PRs__ se eles cumprem com os requisitos descritos e se ele segue a folha de estilo proposta.

### Uso de Issues

As issues do github serão usadas para se ter um maior controle sobre o que se é desenvolvido as issues representarão as histórias de usuário. 

Será cadastrada as tasks e os critérios de aceitação de cada história de usuário seguindo o __template__ definido, além dessa ser especificada em voz de usuário. A especificação da história de usuário seguirá o seguinte padrão: Eu, como <usuário> desejo <meta/desejo>, para <benefício>.

* Exemplo: “Eu, como gerente, desejo cadastrar novos produtos, para manter meu estoque sempre atualizado.”

O nome das issues seguirão o seguinte padrão: <Tipo de Issue> - < Nome definido para a história pela equipe >.
s
* Exemplo : "Feature - Register Product".

<br>

## Necessidades e técnicas para comunicação entre as partes interessadas
<br>


## Linha de base do escopo
<br>

### EEP - Especificação do Escopo do Projeto
<br>

### EAP - Estrutura Analítica do Projeto

<iframe width="1100" height="500" frameborder="0" src="https://www.mindmeister.com/maps/public_map_shell/1242219680/eap-por-reas?width=1100&height=500&z=auto" scrolling="no" style="overflow: hidden; margin-bottom: 5px;">Your browser is not able to display frames. Please visit <a href="https://www.mindmeister.com/1242219680/eap-por-reas2 target="_blank">Hubcare</a> on MindMeister.</iframe>

### EAE - Estrutura Analítica de Entregas

## CRO - Cronograma
<br>

## LBCS - Linha de Base dos Custos
<br>