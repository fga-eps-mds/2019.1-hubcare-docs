# Architecture Document

## Introdução

### Propósito
Este decumento tem como objetivo especificar a arquitetura a ser empregada no projeto HubCare, assim como as tecnologias e
funções deste plug-in para o GitHub utilizado no navegador Google Chrome.

### Escopo
Este documento descreve o HubCare, um plug-in utilizado na web e a arquitetura utilizada é representada de forma sistêmica.

### Definições e palavras de referência
link -> Documento de visão

>API: Interface entre aplicação e programação, gerando comunicação entre sistemas. Utilizada em relação aos microserviços do projeto.
>4+1: Modelo de visualização que descreve a arquitetura do sistema de software baseado em multíplos views paralelos.
>Chrome extension: Um pequeno módulo de software para personalizar o navegador Google Chrome.

### Apresentação arquitetural
Este documento apresenta o sistema de arquitetura no formato 4+1 view. Este formato inclui:
>Logical view
>Process view
>Development view
>Physical view
>Use-case view(Scenarios) 

Este sistema de visualizaçãoe está fortemente ligado à representação por UML.

## Arquitetura do processo

### Diagrama de relações:

![Gras^[Fonte: Do_autor]](images/Gras.png)

### Metodologia

### Design do processo arquitetural
Microsserviços - Abordagem que desenvolve uma única aplicação em uma suite de pequenos serviços.

## Metas e restrições de arquitetura
Tecnologias envolvidas.

HTML/CSS - Utilizado no desenvolvimento Web de forma padrão e estruturado.
JavaScrip - Utilizado no desenvolvimento Web de forma dinâmica.
Python - Linguagem utilizada no desenvolvimento back-end da aplicação.
Django - Framework de desenvolvimento para web que faz uso do padrão model-template-view.
Docker - Tecnologia de fornecimento de contêineres, adicionando uma camada de abstração, automação e virtualização ao S.O.
Google Chrome - Navegador para aplicação do plug-in.

## Visão de implementação
Os dados serão modelados através de UML.
Os pacotes terão caminhos no front-end e back-end .

## Pipeline
CJJCastro

## Bibliografia