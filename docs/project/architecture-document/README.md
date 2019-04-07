# Documento de arquitetura

## Histórico de Revisões

| Data | Versão | Descrição | Autor |
| :--: | :----: | :-------: | :---: |
|  30/03/2019    | 0.1    | Criação do documento e introdução | Vitor Alves e Vitor Meireles |
|  03/04/2019 | 0.2 | Adição de Restrições da Arquitetura  |  Vitor Meireles |
| 04/04/2019 | 0.3 | Adição da Representação da Arquitetura | Rômulo Souza e Vitor Meireles
| 07/04/2019 | 0.4 | Adição do Sumário | Rômulo Souza

## Sumário

- [Documento de arquitetura](#documento-de-arquitetura)
  - [Histórico de Revisões](#hist%C3%B3rico-de-revis%C3%B5es)
  - [Sumário](#sum%C3%A1rio)
  - [1. Introdução](#1-introdu%C3%A7%C3%A3o)
    - [1.1. Finalidade](#11-finalidade)
    - [1.2. Escopo](#12-escopo)
    - [1.3. Definições, Acrônimos e Abreviações](#13-defini%C3%A7%C3%B5es-acr%C3%B4nimos-e-abrevia%C3%A7%C3%B5es)
    - [1.4. Visão geral](#14-vis%C3%A3o-geral)
  - [2. Representação da Arquitetura](#2-representa%C3%A7%C3%A3o-da-arquitetura)
    - [2.1. Django Rest Framework](#21-django-rest-framework)
    - [2.2. Plugin Google Chrome](#22-plugin-google-chrome)
    - [2.3 API GitHub](#23-api-github)
  - [3. Metas e Restrições de Arquitetura](#3-metas-e-restri%C3%A7%C3%B5es-de-arquitetura)
  - [4. Visão lógica](#4-vis%C3%A3o-l%C3%B3gica)
    - [4.1. Diagrama de Classes](#41-diagrama-de-classes)
  - [5. Arquitetura dos Serviços](#5-arquitetura-dos-servi%C3%A7os)
  - [6. Visão de Implementação](#6-vis%C3%A3o-de-implementa%C3%A7%C3%A3o)
    - [6.1. Django Rest Framework](#61-django-rest-framework)
    - [6.2. Plugin Google Chrome](#62-plugin-google-chrome)
  - [7. Referências Bibliográficas](#7-refer%C3%AAncias-bibliogr%C3%A1ficas)

## 1. Introdução

### 1.1. Finalidade

Este documento tem como objetivo descrever a arquitetura do plugin Hubcare. Ele apresenta as decisões de arquiterura para o projeto de forma objetiva e clara e também contém informações que servem de guia para desenvolvedores e gestores compreenderem o fluxo de informações e tecnologias envolvidas.

### 1.2. Escopo

Esse documento demostra as decisões tomadas sobre a organização arquitetural do Hubcare. Estão descritos neste documento: padrões adotados, __frameworks__ e linguagens escolhidas.

### 1.3. Definições, Acrônimos e Abreviações

* API - Application Programming Interface: conjunto de rotinas e padrões estabelecidos por um software para a utilização das suas funcionalidades por demais aplicativos que desejam utilizar seu serviço
* DRF - Django Rest Framework: framework de python utilizado para construção de web APIs
* MVC - Model View Controller: padrão de arquitetura de software constituído por três camadas
* DOM - Document Object Model: plataforma e interface que permite programas a acessar e atualizar o conteúdo, a estrutura e o estilo de um documento

### 1.4. Visão geral

O documento detalha a arquitetura utilizada no projeto. Para isso, é explicada a arquitetura individual dentro de cada tecnologia escolhida e como estas se encaixam no contexto. Depois do entendimento de cada tecnologia, é abordada uma visão lógica do projeto e, uma visão geral representando todo fluxo de informações dentro do Hubcare, bem como todos os serviços utilizados e a visão de implementação dentro de cada tecnologia.

## 2. Representação da Arquitetura

### 2.1. Django Rest Framework

O DRF é um extensão do Django Framework e é utilizado para a construção de APIs em plataforma Web. Com esse, é possível criar um backend independente, através de microsserviços, podendo se comunicar com um front-end de uma aplicação mobile ou web através de arquivos JSON. Uma arquitetura REST opera através de métodos de protocolo HTTP; como GET, POST, PUT, DELETE, entre outros.

A arquitetura do DRF é baseada na arquitetura MVC, onde a camada da controller ocorre internamente ao framework, de forma automática. No Hubcare, cada funcionalidade é representada por um app interno, para melhor modularização do sistema. Além disso, app contém sua model e suas views. Isso pode ser melhor observado na [Visão de implementação]()

A model do DRF é a camada responsável por gerir, modelar e persistir os dados. Tem   como principais funções controlar o estado dos dados, responder a instruções para mudança de estado dos dados, cuidar das regras de negócio da aplicação e controlar as transações com o banco de dados da aplicação.

A view do DRF é a camada encarregada por interpretar entradas vindas de outros sistemas (através de endpoints), distribuindo comandos que geram atualização, busca de dados ou requisições em outras partes do próprio sistema ou de outro sistema que esteja sendo consumido, fazendo o uso das classes definidas na camada de modelo(Model).


### 2.2. Plugin Google Chrome

Plugins para o google chrome são pequenos programas utilizados para customizar a experiência de um usuário ao ulitizar o browser. São extensões que permitem a utilização de novas funcionalidades.

Os plugins são feitos em tecnologias web, como HTML, CSS e JavaScript. No Hubcare, o plugin será responsável por trocar informações com o backend e mostrá-las na página acessada pelo usuário. Para isso, deve editar o conteúdo HTML presente na página, acrescentando as informações recebidas pelo backend.A arquitetura do plugin é composta por 4 componentes: popup.html, popup.js, background.js e contentscript.js.

* Popup.html - janela feita em HTML que sobrepõe o conteúdo da página
* Popup.js - controla as funcionalidades da popup.html
* Background.js - script responsável pelos eventos que ocorrem na página e precisam ser observados pelo plugin. O módulo background deve ficar desabilitado quando não é utilizado, e carregado apenas quando necessário.
* Contentscript.js - responsável pela leitura e escrita em uma página web. Ele lê e modifica o DOM de páginas web acessadas pelo browser.

<img alt="chrome-architecture" src="../../images/default/chrome-architecture.png" />

### 2.3 API GitHub

A API do GitHub é consumida pelo backend do Hubcare. Os dados advindos da API são processados de acordo com os critérios adotados, presentes no [plano de medição](), gerando as métricas desejadas, que retornarão ao plugin do Chrome.

## 3. Metas e Restrições de Arquitetura

Tecnologias utlizadas para o desenvolvimento:

* HTML/CSS - Utilizado no desenvolvimento Web de forma padrão e estruturado.
* JavaScrip - Utilizado no desenvolvimento Web de forma dinâmica.
* Python - Linguagem utilizada no desenvolvimento backend da aplicação.
* Django - Framework de desenvolvimento para web que faz uso do padrão model-template-view.
* Docker - Tecnologia de fornecimento de contêineres, adicionando uma camada de abstração, automação e virtualização ao S.O.
* Google Chrome - Navegador para aplicação do plugin.

O Pluguin Hubcare possui as seguintes restrições de arquitetura:

* Versão do plugin apenas para o Google Chrome
* Número de requisições feitas para a API do GitHub limitam-se a 60 quando não autenticado, e a 5000 quando autenticado

## 4. Visão lógica

### 4.1. Diagrama de Classes

![diagrama_classes](../../images/default/diagrama_classes.jpg)

## 5. Arquitetura dos Serviços 

![arquitetura](../../images/default/eps_architecture.png)

## 6. Visão de Implementação

### 6.1. Django Rest Framework

No projeto, cada tema estará definido por um app do django. Os apps são separados por issues, pull requests e community, por serem as principais divisões que estão contidas nas métricas escolhidas para a avaliação de um repositório. Além disso, cada app é composto pelos seguintes arquivos:

* **models.py** - implementa a camada model e as validações personalizadas dos dados que serão guardados no banco de dados
* **views** - pasta que contém todas as views relacionadas ao app
* **views.py** - implementa a camada view, que é responsável pela interação com a model e por processar todos os dados advindos da API do GitHub
* **urls.py** - endpoints que permitem acesso às views
* **serializers.py** - responsável por serializar dados - convertê-los de objeto para JSON - e também por validá-los de acordo com os dados da modelo

### 6.2. Plugin Google Chrome

No hubcare, a popup.html será apenas uma pequena janela responsável por habilitar e desabilitar o plugin e ficará visível ao ser clicada pelo usuário.

O contentscript é a parte principal da aplicação. Ele receberá as métricas providas pelo backend e as apresentará dentro da aba **Hubcare**, que o próprio plugin irá criar.


## 7. Referências Bibliográficas

>Definição de DOM pela w3school. Disponível em: https://www.w3schools.com/js/js_htmldom.asp. Acesso em: 04 abr. 2019.

>Documentação oficial do Django. Disponível em: https://www.djangoproject.com/. Acesso em: 04 abr. 2019

>Documentação oficial do Django Rest Framework. Disponível em: https://www.django-rest-framework.org/. Acesso em: 04 abr. 2019.

>Tutorial sobre plugin do chrome para desenvolvedores. Disponível em: https://developer.chrome.com/extensions/overview. Acesso em: 04 abr. 2019.
