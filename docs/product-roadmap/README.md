# Roadmap de Produto

**Autor: Filipe Toyoshima**

## Introdução

O Roadmap de Produto, em termos tradicionais, é um documento que exibe um caminho, uma sequência de atividades ao longo do tempo para que o produto ao qual se refere seja entregue em um determinado escopo de tempo.

Normalmente, o Roadmap é uma das formas de se planejar o produto, desde sua concepção até sua finalização. Entretanto, isso nos lembra muito os métodos tradicionais de Engenharia de Software, onde há uma sequência de passos pré-determinados que levam ao objetivo final do projeto. Não é assim que se trabalha nas metodologias ágeis.

Para elaboração do produto deste projeto, serão utilizados alguns dos princípios Lean, ilustrados brilhantemente pelo [blog Toggl](https://toggl.com/developer-methods-infographic/).

![Características do Lean](lean.png)

Uma outra ilustração um pouco menos jocosa (mas não tão pouco) sobre os princípios Lean foi usada por [Jeff Gothelf](https://www.jeffgothelf.com/blog/), autor de *Lean UX*, em seu [artigo na Medium](https://medium.com/@jboogie/what-does-an-agile-product-roadmap-look-like-cf0dbe5be4ef):

![Ilustração do Jeff](https://cdn-images-1.medium.com/max/800/1*XpFXZzvJc3zwmFMPhlWjoQ.png)

Visto isso, nota-se um planejamento a longo prazo em termos de features do produto não se faz necessários, podendo até mesmo ser um erro, uma vez que o produto aqui descrito se trata de uma inovação.

*Erre, mas erre cedo!*

Uma vez que os erros foram cometidos, é necessários entendê-los aprender com eles.

![Loop do Lean](lean-loop.png)

Pensando nisso, temos que planejar por onde começar a errar, para que as experimentações sejam significativas para a validação e construção de um produto de qualidade para o usuário.

## Roadmap Inicial

O planejamento conta com passos de alto nível de abstração, que se referem a outras partes do projeto já documentadas.

<iframe frameborder="0" style="width:100%;height:2114px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&layers=1&nav=1&title=Product%20Roadmap.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1LfVQUN_wz5rKCXMoNggUARRcwP3ucQ3m%26export%3Ddownload"></iframe>

O Roadmap é dividio em três níveis: planejamento, preparação, e pivotagem. Quanto mais se desce no diagrama, mais maleáveis são as ideias.

### Planejamento

O planejamento se refere a entender os objetivos finais do projeto, aquilo que tem que ser alcançado.

Inicia-se com a visão, descrita em mais detalhes no [Documento de Visão](https://fga-eps-mds.github.io/2019.1-hubcare-docs/project/vision-document/). Essa visão refere-se à parte mais rígida do planejamento, pois se a visão do produto se altera um pouco, todo o resto terá que se adequar.

Para alcançar a visão, foram separados quatro objetivos. Assim como na visão, todo o resto é pensado com base neles.

Como o projeto se trata de entender um domínio, que é a saúde de repositórios, faz sentido incluir, ainda na fase de planejamento, a elaboração de um [Plano de Medição](https://fga-eps-mds.github.io/2019.1-hubcare-docs/project-quality-management/measurement-model/).

### Preparação

A preparação se refere a montar a estrutura para que possam se iniciar a pivotagem. Como o projeto deverá prover uma visão para usuários do GitHub, planejar a estrutura para editar páginas do site será essencial para os primeiros testes.

Os requisitos considerados de maior relevância para a API que realizará as requisições e para o Plugin que modificará as páginas do GitHub já se encontram documentadas. O serviço gerador de gráficos foi postergado para depois da primeira pivotagem, pois se mostra uma feature mais difícil de ajustar.

### Pivotagem

A pivotagem é um passo essencial no Lean, pois se trata de verificar se a solução realizada atende os objetivos propostos e, também, se os objetivos contemplam a visão do projeto.

A primeira pivotagem se refere às badges que resumem a qualidade de um repositório. Através disso, é possível verificar se a solução de modificar as páginas do GitHub agrada os usuários.

Um plano de Teste de Aceitação ainda será planejamento.

### Próximas Etapas

Por mais que o Lean concentre-se em planejar as coisas aos poucos para que não se tomem decisões comprometedoras das quais o time pode se arrepender posteriormente, é importante elicitar no roadmap quais são as possíveis features que resolverão objetivos ainda não contemplados na primeira pivotagem.

Depois da primeira pivotagem planejada, ainda restará um objetivo para ser concluído, que podederá ser resolvido através de auxílio de gráficos gerados por um serviço à parte, linkados através de *iframes* HTML.

É claro que a execução dessa parte do trabalho é dependente dos resultados da primeira pivotagem, mas a expectativa é que as alterações no que foi planejado para teste inicial sejam pequenas e que o time possa trabalhar em paralelo nessas alteraçõe e nas features que serão incluídas para as próximas.