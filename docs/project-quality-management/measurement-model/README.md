# Modelo de Medição de Repositórios do GitHub

**Autor: Filipe Toyoshima**

## Introdução

Como consta em [Documento de Visão](../../project/vision-document/README.md), o objetivo deste software é ajudar a comunidade do GitHub a aferir a saúde de repositórios com dois fins:

- Saber se usuários do software alocado no repositório vão ter suporte da comunidade ou dos mantenedores
- Saber se vale a pena começar a contribuir com a comunidade presente no repositório

Pensando nisso, o time de desenvolvimento elaborou um plano de medição no modelo [GQM](https://pt.wikipedia.org/wiki/GQM). O modelo consiste em três níveis de abstração: Conceitual, que contém o objetivo de medição; Operacional, que contém questões que ajudar a carcterizar o objeto de medição; e Quantitativo, que tem por objetivo responder as questões do nível Operacional.

Obs: Por mais que o objetivo deste projeto de software seja auxiliar usuários do GitHub, o plano de medição foi desenhado para que possa ser escalado para outras plataformas que hospedem softwares livres versionados através de Git, como o GitLab por exemplo.

### Visão Geral

<iframe frameborder="0" style="width:100%;height:487px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=GQM%20Sa%C3%BAde%20do%20Reposit%C3%B3rio.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1b0XRy3ICahhu0ra5ZUOjQIfL2gtCFSEK%26export%3Ddownload"></iframe>

## Nível Conceitual - Os Objetivo de Medição

Analisar repositórios do GitHub com o propósito de aferir a saúde dos mesmos caracterizada pela atividade do repositório e receptividade com novos colaboradores e usuário. Essa análise deverá ocorrer sob o ponto de vista de usuários e das plataformas de Software aberto no contexto de quem procura repositórios para utilizar e contribuir as ferramentas disponíveis.

## Nível Operacional - As Questões

Os usuários das plataformas podem ser caracterizados em dois: usuários e contribuidores. Podem ainda existir usuários que se enquadrem em ambas as categorias.

**Questão 1** - Para ambas as categorias, convém ainda saber sobre o quão ativo está uma comunidade sobre um software. Um software que não é mais mantido não oferecerá suporte e nem receberá nenhum novo contribuidor.

**Questão 2** - Para contribuidores em potencial que ainda não conhecem um software, convém saber sobre a receptividade de determinada comunidade.

**Questão 3** - Para os usuários, convém querer saber sobre o suporte que eles podem obter da comunidade que mantém determinado software.

A resposta para cada questão se dará num número que varia de 0 a 1 resultante da média ponderada das métricas abaixo, de acordo com o peso predeterminado para cada questão.

## Nível Quantitativo - As Métricas

### M1 - Quantidade de Commits no último mês

Nome autoexplicativo, medirá a quantidade de commits realizado nos últimos 30 dias.

#### Medida

A medida deverá seguir a seguinte fórmula.

`0.1 * Qtd_de_Commits`

O maior resultado possível é 1, de tal maneira que para qualquer valor de `Qtd_de_Commits` igual ou maior que 10, o resultado sempre será 1.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 1 | 3 |

### M2 - Qualidade de Aceitação de Pull Requests

Métrica referente ao quão bem a comunidade vem trabalhando com Pull Requests. Para obter essa avaliação de qualidade, deverá considerar se o Pull Request em questão foi aceito ou recusado e se teve discussão recente.

Considera-se "PR com discussão recente" aquele que teve algum comentário nos últimos 15 dias.

#### Amostra

A opção que oferecer *menos* Pull Requests:

- Pull Requests que foram abertos nos últimos 60 dias
- Últimos 50 Pull Requests

#### Medida

Cada PR avaliado deve estar em uma das seguintes categorias:

| Situação | Discussão | Resultado |
| :------: | :-------: | :-------: |
| Merjado | Sim | 1 |
| Merjado | Não | 0.9 |
| Aberto | Recente (<=15 dias) | 0.9 |
| Fechado e sem Merge | Sim | 0.7 |
| Aberto | Antiga (>15 dias) | 0.3 |
| Fechado e sem Merge | Não | 0.1 |
| Aberto | Não / antiga | 0 |

A medida será a média dos resultados obtidos em cada PR.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 1 | 2 |
| 2 | 3 |

### M3 - Quantidade de Contribuídores Diferentes no Último Mês

#### Amostra

Commits realizados nos últimos 30 dias.

#### Medida

A medida será calculada com base na quantidade de autores únicos dentro da amostra.

`0.25 * Qtd_de_Autores`

O resultado máximo para a equação deve ser 1, assim, para qualquer quantidade de autores maior ou igual a 4, o resultado sempre deverá ser 1.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 1 | 1 |
| 2 | 2 |

### M4 - Presença de Release Notes

#### Amostra

Release Notes dos últimos 90 dias.

#### Medida

Se tiver uma Release Note, será 1. Caso contrário, será 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 1 | 1 |
| 3 | 3 |

### M5 - Taxa de Issues Ativas

#### Amostra

Todas as Issues abertas do repositório.

#### Medida

`((qtd_issues_ativas / qtd_issues_abertas)-0.5)*4`

Onde uma issue ativa significa uma issue que tenha tido alguma atividade no últimos 15 dias.

Lembrando que o valor máximo da métrica deve ser 1 e o valor mínimo deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 1 | 3 |
| 2 | 2 |
| 3 | 3 |

### M6 - Presença de Guia de Contribuição

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 3 |

### M7 - Taxa de Issues marcadas com "help wanted"

#### Amostra

Todas as issues abertas do repositório.

#### Medida

Tx = Issues Marcadas com "Help Wanted" / Amostra total

`(Tx - 0.04) * 25`

O resultado máximo para a equação deve ser 1, assim, para qualquer quantidade de autores maior ou igual a 0.08, o resultado sempre deverá ser 1.

O mesmo é válido para o valor mínimo, 0, para qualquer Tx menor ou igual a 0.04.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 3 |

### M8 - Taxa de Issues marcadas com "good first issue"

#### Amostra

Todas as issues abertas do repositório.

#### Medida

Tx = Issues Marcadas com "good first issue" / Amostra total

`(Tx - 0.04) * 25`

O resultado máximo para a equação deve ser 1, assim, para qualquer quantidade de autores maior ou igual a 0.08, o resultado sempre deverá ser 1.

O mesmo é válido para o valor mínimo, 0, para qualquer Tx menor ou igual a 0.04.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 3 |

### M9 - Presença de Pull Request Template

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 2 |

### M10 - Presença de ReadMe

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 3 |
| 3 | 3 |

### M11 - Presença de Issue Template

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 2 |
| 3 | 2 |

### M12 - Presença de Licença

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 1 |
| 3 | 3 |

### M13 - Presença de Código de Conduta

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 3 |
| 3 | 1 |

### M14 - Presença da Descrição do Repositório

#### Medida

Se o artefato existir, a medida deve ser 1, caso contrário, deve ser 0.

#### Relevância para as questões

| Questão | Peso |
| ---:| :---:|
| 2 | 1 |
| 3 | 1 |

## Resumo da Ponderação

Segue resumo dos pesos de cada métrica atribuídos para cada questão.

| Métrica | Questão 1 | Questão 2 | Questão 3 |
| ------: | :-------: | :-------: | :-------: |
| M1 | 3 | 0 | 0 |
| M2 | 2 | 3 | 0 |
| M3 | 1 | 2 | 0 |
| M4 | 1 | 0 | 3 |
| M5 | 3 | 2 | 3 |
| M6 | 0 | 3 | 0 |
| M7 | 0 | 3 | 0 |
| M8 | 0 | 3 | 0 |
| M9 | 0 | 2 | 0 |
| M10 | 0 | 3 | 3 |
| M11 | 0 | 2 | 2 |
| M12 | 0 | 1 | 3 |
| M13 | 0 | 3 | 1 |
| M14 | 0 | 1 | 1 |

## Evoluções Futuras

Esse documento se trata de uma primeira versão, destinada a servir como base para um MVP - Produto minimamente viável - do Projeto de Software em questão.  Tanto que, nessa versão, as métricas estão classificadas como "boa", "ruim" e similares, sem uma quantificação objetiva, como seria apropriado. Mas vai rolar.

Algumas evoluções ainda podem ser feitas, embora não sejam prioridade no momento de construção desse documento.

- A Métrica 5 (Taxa de Isses Ativas) tem por objetivo analisar como a comunidade lida com as issues. No entanto, Issues podem ser ignoradas e fechadas, o que mascararia a métrica. A equipe reconheceu que completar a métrica para uma melhor análise seria de uma complexidade muito algo para uma correção que não é prioridade no momento.
- É interessante analisar como as issues são tratadas quando se leva em consideração quem as criou. Um repositório com issues da comunidade geralmente é melhor do que um apenas com issues dos mantenedores.
- A análise do README é muito rasa. Apenas existir um arquivo chamado README na pasta raiz não diz muita coisa. É cabível uma análise textual. Porém, isso demandaria um trabalho de Machine Learning, o que aumentaria demais a complexidade por agora.

Além disso, as métricas foram construídas e classificadas com base na experiência do time responsável, sem qualquer consulta bibliográfica mais aprofundada. Reconhecemos esse fato como um risco. Por isso, o módulo do software responsável pelas equações e conclusões será feito de tal modo que o ajuste de parâmetros seja o mais fácil possível, pois ainda existe a pretensão de uma pesquisa mais fundamentada.