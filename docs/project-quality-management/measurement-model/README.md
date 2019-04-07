# Modelo de Medição de Repositórios do GitHub

**Autor: Filipe Toyoshima**

## Introdução

Como consta em Documento de Visão, o objetivo deste software é ajudar a comunidade do GitHub a aferir a saúde de repositórios com dois fins:

- Saber se usuários do software alocado no repositório vão ter suporte da comunidade ou dos mantenedores
- Saber se vale a pena começar a contribuir com a comunidade presente no repositório

Pensando nisso, o time de desenvolvimento elaborou um plano de medição no modelo [GQM](https://pt.wikipedia.org/wiki/GQM). O modelo consiste em três níveis de abstração: Conceitual, que contém o objetivo de medição; Operacional, que contém questões que ajudar a carcterizar o objeto de medição; e Quantitativo, que tem por objetivo responder as questões do nível Operacional.

Obs: Por mais que o objetivo deste projeto de software seja auxiliar usuários do GitHub, o plano de medição foi desenhado para que possa ser escalado para outras plataformas que hospedem softwares livres versionados através de Git, como o GitLab por exemplo.

### Visão Geral

![Diagrama do GQM]({{ site.url }}/images/charts/gqmChart.png)

## Nível Conceitual - Os Objetivo de Medição

Analisar repositórios do GitHub com o propósito de aferir a saúde dos mesmos caracterizada pela atividade do repositório e receptividade com novos colaboradores e usuário. Essa análise deverá ocorrer sob o ponto de vista de usuários e das plataformas de Software aberto no contexto de quem procura repositórios para utilizar e contribuir as ferramentas disponíveis.

## Nível Operacional - As Questões

Os usuários das plataformas podem ser caracterizados em dois: usuários e contribuidores. Podem ainda existir usuários que se enquadrem em ambas as categorias.

**Questão 1** - Para ambas as categorias, convém ainda saber sobre o quão ativo está uma comunidade sobre um software. Um software que não é mais mantido não oferecerá suporte e nem receberá nenhum novo contribuidor.

**Questão 2** - Para contribuidores em potencial que ainda não conhecem um software, convém saber sobre a receptividade de determinada comunidade.

**Questão 3** - Para os usuários, convém querer saber sobre o suporte que eles podem obter da comunidade que mantém determinado software.

## Nível Quantitativo - As Métricas

### M1 - Quantidade de Commits no último mês

Nome autoexplicativo, medirá a quantidade de commits realizado nos últimos 30 dias.

#### Medida

| Qtd de Commits | Resultado |
| :------------: | :-------: |
| 10 ou mais     | Satisfatório|
| entre 9 e 1    | Mediano   |
| 0              | Ruim      |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Alta |

### M2 - Qualidade de Aceitação de Pull Requests

Métrica referente ao quão bem a comunidade vem trabalhando com Pull Requests. Para obter essa avaliação de qualidade, deverá considerar se o Pull Request em questão foi aceito ou recusado e se teve discussão recente.

Considera-se "PR com discussão recente" aquele que teve algum comentário nos últimos 15 dias.

#### Amostra

A opção que oferecer *menos* Pull Requests:

- Pull Requests que foram abertos nos últimos 60 dias
- Últimos 50 Pull Requests

#### Medida

| Situação | Discussão | Resultado |
| :------------: | :-------: | :---:|
| Aceito | Sim | Excelente |
| Aceito | Não | Bom |
| Aberto | Recente | Bom |
| Recusado | Sim | Rasoável |
| Recusado | Não | Ruim
| Aberto | Não / antiga | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Média |
| 2 | Alta  |

### M2 - Qualidade de Aceitação de Pull Requests

Métrica referente ao quão bem a comunidade vem trabalhando com Pull Requests. Para obter essa avaliação de qualidade, deverá considerar se o Pull Request em questão foi aceito ou recusado e se teve discussão recente.

Considera-se "PR com discussão recente" aquele que teve algum comentário nos últimos 15 dias.

#### Amostra

A opção que oferecer *menos* Pull Requests:

- Pull Requests que foram abertos nos últimos 60 dias
- Últimos 50 Pull Requests

#### Medida

| Situação | Discussão | Resultado |
| :------------: | :-------: | :---:|
| Aceito | Sim | Excelente |
| Aceito | Não | Bom |
| Aberto | Recente | Bom |
| Recusado | Sim | Rasoável |
| Recusado | Não | Ruim
| Aberto | Não \|\| Antiga | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Média |
| 2 | Alta  |

### M3 - Quantidade de Contribuídores Diferentes no Último Mês

#### Amostra

Commits realizados nos últimos 30 dias.

#### Medida

A medida será calculada com base na quantidade de autores únicos dentro da amostra.

| Qtd de Autores | Resultado |
| :------------: | :-------: |
| 4 ou mais | Aceitável |
| entre 3 e 1 | Mediano |
| 0 | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Baixa |
| 2 | Média |

### M4 - Presença de Release Notes

#### Amostra

Release Notes dos últimos 90 dias.

#### Medida

| Qtd Release Notes | Resultado |
| :------------: | :-------: |
| 1 ou mais | Bom |
| 0 | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Baixa |
| 3 | Alta |

### M5 - Taxa de Issues Ativas

#### Amostra

Todas as Issues abertas do repositório.

#### Medida

Tx = Issues ativas / Amostra

| Tx | Resultado |
| :------------: | :-------: |
| 75% ou maior | Bom |
| entre 75% e 50% | Mediana |
| menor que 50% | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 1 | Alta |
| 2 | Média|
| 3 | Alta |

### M6 - Presença de Guia de Contribuição

#### Medida

| Guia de Contribuição | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Alta |

### M7 - Taxa de Issues marcadas com "help wanted"

#### Amostra

Todas as issues abertas do repositório.

#### Medida

Tx = Issues Marcadas com "Help Wanted" / Amostra total

| Tx | Resultado |
| :------------: | :-------: |
| 10% ou mais | Bom |
| entre 10% e 5% | Mediano |
| abaixo de 5% | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Alta |

### M8 - Taxa de Issues marcadas com "good first issue"

#### Amostra

Todas as issues abertas do repositório.

#### Medida

Tx = Issues Marcadas com "good first issue" / Amostra total

| Tx | Resultado |
| :------------: | :-------: |
| 10% ou mais | Bom |
| entre 10% e 5% | Mediano |
| abaixo de 5% | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Alta |

### M9 - Presença de Pull Request Template

#### Medida

| PR Template | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Média |

### M10 - Presença de ReadMe

#### Medida

| README | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Alta |
| 3 | Alta |

### M11 - Presença de Issue Template

#### Medida

| Issue Temaplate | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Média |
| 3 | Média |

### M12 - Presença de Licença

#### Medida

| Licença | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Baixa |
| 3 | Alta |

### M13 - Presença de Código de Conduta

#### Medida

| Código de Conduta | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Alta |
| 3 | Baixa |

### M14 - Presença da Descrição do Repositório

#### Medida

| Descrição | Resultado |
| :------------: | :-------: |
| Existe | Bom |
| Não existe | Ruim |

#### Relevância para as questões

| Questão | Relevância |
| ---:| :---:|
| 2 | Baixa |
| 3 | Baixa |

## Evoluções Futuras

Esse documento se trata de uma primeira versão, destinada a servir como base para um MVP - Produto minimamente viável - do Projeto de Software em questão.  Tanto que, nessa versão, as métricas estão classificadas como "boa", "ruim" e similares, sem uma quantificação objetiva, como seria apropriado. Mas vai rolar.

Algumas evoluções ainda podem ser feitas, embora não sejam prioridade no momento de construção desse documento.

- A Métrica 5 (Taxa de Isses Ativas) tem por objetivo analisar como a comunidade lida com as issues. No entanto, Issues podem ser ignoradas e fechadas, o que mascararia a métrica. A equipe reconheceu que completar a métrica para uma melhor análise seria de uma complexidade muito algo para uma correção que não é prioridade no momento.
- É interessante analisar como as issues são tratadas quando se leva em consideração quem as criou. Um repositório com issues da comunidade geralmente é melhor do que um apenas com issues dos mantenedores.
- A análise do README é muito rasa. Apenas existir um arquivo chamado README na pasta raiz não diz muita coisa. É cabível uma análise textual. Porém, isso demandaria um trabalho de Machine Learning, o que aumentaria demais a complexidade por agora.

Além disso, as métricas foram construídas e classificadas com base na experiência do time responsável, sem qualquer consulta bibliográfica mais aprofundada. Reconhecemos esse fato como um risco. Por isso, o módulo do software responsável pelas equações e conclusões será feito de tal modo que o ajuste de parâmetros seja o mais fácil possível, pois ainda existe a pretensão de uma pesquisa mais fundamentada.