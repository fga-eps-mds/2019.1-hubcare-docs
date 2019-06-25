# Teste de Aceitação 1

**Autor: Filipe Toyoshima**

## Introdução

Este documento visa expor os resultados adquiridos durante a segunda baterira de testes de aceitação do Projeto Hubcare. Os testes seguem parcialmente o [modelo de testes](../../acceptance-test-model/README.md), pois a falta de recursos impede uma realização completa. De qualquer forma, os testes não devem ser negligenciados, pois visam validar se o atual estado do projeto é capaz de atender sua [visão](../../../project/vision-document/README.md).

| | |
| -- | -- |
| Data dos Testes | 24/06/2019 |
| Versão testada | 1.1 |

## Escopo

A versão a ser testada conta com todo o escopo previso no início do projeto. Em resumo, inclui as badges com a pontuação e um relatório completo em cada uma das três categorias calculadas. Os relatórios contam com gráficos e barras de progresso.

Além disso, há também um Popup que aparece ao clicar no botão do HubCare, adicionado no próprio Google Chrome. Esse Popup contém:

- uma breve descrição do que é levado em consideração para o cálculo de cada uma das badges.
- um switch para ativar e desativar o plugin, sem necessariamente desativá-lo do navegador
- um botão de login para autenticação do usuário

## Metodologia

Os testes ocorreram de duas formas diferentes. Em uma delas, o Hubcare já se encontrava instalado na máquina dos facilitadores e lá foram realizados os testes. Na outra, existia a versão do Hubcare na Chrome Store estava atualizada e os usuários puderam instalar o Hubcare em suas próprias máquinas.

Foi explicado bem brevemente a que o Hubcare se propunha, mas foi pedido aos próprios usuários que entendessem o que exatamente era levado em consideração para que as notas fossem calculadas. Além disso, não houveram quaisque instruções a respeito de como usar a ferramenta, a não ser em caso de problemas adversos à aplicação, como os de conexão.

Como tarefa de uso, os usuários foram solicitados a pesquisarem repositórios de sua preferência que fossem semelhantes e tentassem, com o auxílio do Hubcare, aferir qual deles seria melhor.

## Teste 1

### Participantes

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |
| Cleber Castro    | DevOps |

### Usuário de Teste

O primeiro usuário de testes se identificou como homem, de 20 anos, de etnia parda/indígena de renda média alta e interessado em desenvolvimento de jogos eletrônicos. Tem alguma experiência com programação e é acostumado com o uso de software livre.

### Comentários do Usuário

Este teste foi realizado na máquina de um membro do time e a etapa de instalação foi pulada.

> Não entendi em um primeiro encontro que eu deveria fazer login, tampouco onde eu deveria fazer o login.

> Não é tão claro o fato de que uma aba Hubcare aparece

> Depois de se entender os fluxos da ferramenta, o que não demora muito tempo, tenho também a sensação de que entendo como cada métrica é calculada e o que eu poderia fazer para aumentar o score

## Teste 2

### Participantes

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |
| Cleber Castro    | DevOps |

### Usuário de Teste

O usuário de testes é um homem de 22 anos, branco, de renda baixa e sem um interesse muito bem definido, apenas gosta de programar. Convive diariamente com as ferramentas de software livre.

### Comentários do Usuário

> Pensei que as badges eram clicáveis. Seria legal se cada uma delas levasse ao seu relatório.

> Não é tão claro o fato de que uma aba Hubcare aparece

> Alguns gráficos ou barras de progresso dos relatórios poderiam ser clicáveis e levar até o dado que está sendo representado

> Achei que o as bordas pretas das barras de progresso sobrecarregam a interface. Só um preenchimento suave talvez ficasse mais agradável.

> A identidade visual dos checks não conversa com as demais páginas.

## Teste 3

### Participante

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |

### Usuária de Teste

A usuária é uma mulher de 24 anos que identifica sua etnia como Preta e sua renda como baixa. Tem interesse na área de gestão de software e lida diariamente com ferramentas de software livre.

### Comentários da Usuária

> Não é claro o que significa "to get a High Score"

> Issue Activity Rate não faz sentido

> O texto do Popup não é atraente, é dispensável. Por causa da não leitura, não ficou claro sobre o que cada métrica falava

> Depois de entender o fluxo de uso, consigo compreender a maioria das métricas e entender a saúde do repositório aferido

## Teste 4

### Participante

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |

### Usuário de Teste

O usuário é um homem de 20 anos, auto identificado como Negro, de renda média, que tem como principal interesse o desenvolvimento de jogos.

### Comentários do Usuário

> No momento da autorização, estou cedendo meus dados para cjjcastro. O que é isso?

> Meu repositório tem PR Template, mas o Hubcare não o identifica

> O ícone do app no Google Chrome não é fácil de encontrar para fazer login.

## Teste 5

### Participante

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |

### Usuário de Teste

O usuário é um homem de 21 anos que identificou sua etnia como Pardo e sua renda como média. Não tem um interesse específico dentro de software, apenas gosta de desenvolver. Está em contato diário com ferramentas de software livre.

### Comentários do Usuário

Não houveram muitas críticas construtivas acerca da aplicação, apenas comentários positivos acerca do visual e fluxo de uso da ferramenta.

## Teste 6

### Participante

| Participante | Papel |
| -- | -- |
| Filipe Toyoshima | Product Manager |

### Usuário de Teste

O usuário é um homem de 21 anos que identificou sua etnia como Branco e sua renda como média alta. Tem interesse em desenvolvimento android e está em contato semanal com ferramentas de software livre.

### Comentários do Usuário

Não houveram muitas críticas construtivas acerca da aplicação, apenas comentários positivos acerca do visual e fluxo de uso da ferramenta.

## Conclusão

**A solução proposta resolve o problema do público-alvo?**

Sim. Apesar de alguns bugs e imperfeições identificadas na aplicação, é possível ter um bom entendimento a respeito da saúde do reposiório que se está aferindo.

**Existe uma maneira melhor de atacar o problema?**

Algumas sugestões de incremento foram dadas, como a de tornar as badges clicáveis, assim como cada métrica do relatório. O time parece estar desenvolvendo a ferramenta no caminho certo para oferecer informações úteis aos usuários.

**O usuário de teste sentiu falta de alguma coisa?**

Sim. Todas as faltas foram listadas nos Comentários. Ênfase nos Testes [2](#comentarios-do-usuario_1) e [3](#comentarios-do-usuario_2)

**O usuário de teste abdicou de usar alguma parte da solução?**

Não. O fluxo a ser testado é bem minimalista.

## Features/Modificações Sugeridas

- Muitos usuários reclamaram a respeito do primeiro contato com a ferramenta. Talvez fosse interessante, logo após o login, levar o usuário até uma página explicativa.
- Badges clicáveis que levem até seus relatórios
- Gráficos e barras de progresso que levem até os dados aos quais se referem
- Mudanças de estilização
- Explicar em maiores detalhes o que é "to get a High Score"
- Alterar processo de autorização de cjjcastro para Hubcare

## Bugs encontrados

- Issue Activity Rate estranho
- O gráfico que mostra os diferentes tipos de PR não aparece quando não existem PRs a serem analizados.
- Padrão de PR Template não identificado