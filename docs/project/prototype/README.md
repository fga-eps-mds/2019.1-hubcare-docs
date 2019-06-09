# Documento de Prototipação de Alta Fidelidade

**[Link to test](https://www.figma.com/proto/InvRd6TLwMWdsIdz5ieEgm23/HubCare-Prototype?node-id=0%3A1&scaling=min-zoom)**

<iframe style="border: none;" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Ffile%2FInvRd6TLwMWdsIdz5ieEgm23%2FHubCare-Prototype%3Fnode-id%3D0%253A1" allowfullscreen></iframe>

---

# Diretrizes Visuais para o HubCare no GitHub

Para o mantenimento de a qualidade do padrão visual de qualquer coisa que o Plugin HubCare renderize dentro da página do GitHub, é necessário estabelecer as diretrizes às quais qualquer elemento visual deva se enquadrar para a entrega de uma parte do produto.

Todas as diretrizes foram inspiradas em elementos já encontrados no GitHub, de modo a diminuir a sensação de estranheza que o usuário possa sentir a ver algo novo dentro de uma página à qual já está acostumado.

## Cores

As cores, em sua maioria, devem ser cores já presentes no GitHub.

### Elementos de Confirmação

Para **elementos de confirmação**, como o sinais de Check, utilize este tom de verde: <span style="color:#28a745;"> #28a745 </span>. Esse é o tom utilizado pelo GitHub para ícones de issues e PRs abertos.

<div style="background-color:#28a745;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #fff;">
        <div style="padding-top: 35%">#28a745</div>
</div>

### Elementos de Falha

Para **elementos de falha**, utilize esse tom de vermelho: <span style="color:#cb2431">#cb2431</span>. Esse é o tom utilizado pelo GitHub para os ícones de issue fechado, por exemplo.

<div style="background-color:#cb2431;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #fff;">
        <div style="padding-top: 35%">#cb2431</div>
</div>

### Elementos relacionados a PR

Para alguns **elementos relacionados a Pull Requests**, pode ainda ser utilizado esse tom de roxo: <span style="color:#6f42c1">#6f42c1</span>. Quase tudo relacionado a PR no GitHub tem esse tom.

<div style="background-color:#6f42c1;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #fff;">
        <div style="padding-top: 35%">#6f42c1</div>
</div>

### Elementos relacionados a commits

Para colorir algum **detalhe referente a commits**, recomenda-se esse tom de laranja: <span style="color:#f66a0a">#f66a0a</span>. O GitHub utiliza esse tom em alguns gráficos referentes a commits.

<div style="background-color:#f66a0a;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #fff;">
        <div style="padding-top: 35%">#f66a0a</div>
</div>

### Linhas divisoras

Para as linhas que marquem as divisórias entre painéis e outros elementos que componham a interface, recomenda-se esse tom de cinza: <span style="color:#d1d5da; background: #000">#d1d5da</span>. Toda divisória do GitHub se encontra nessa cor.

<div style="background-color:#d1d5da;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #000;">
        <div style="padding-top: 35%">#d1d5da</div>
</div>

**Obs:** Não atentar apenas às cores, mas também ao estilo.

<div style="border-radius: 3px;
            border: 1px solid;
            border-color: #d1d5da;
            margin: auto;
            text-align: center;
            width:230px">
    <div style="margin: 2px">
        <p>border-radius: 3px;</p>
        <p>border: 1px solid;</p>
        <p>border-color: #d1d5da</p>
    </div>        
</div>

### Fundo Escuro

Alguns elementos do GitHub, como headers de tabelas, exigem um fundo um pouco mais escuro que o branco, para que se tenha uma ideia de diferenciação. Para isso, recomenda-se esse tom: <span style="color:#f6f8fA; background: #000">#f6f8fa</span>.

<div style="background-color:#f6f8fa;
            width:80px;
            height:80px;
            border-radius: 50px;
            margin: auto;
            text-align: center;
            color: #000;
            border:1px solid;
            border-color: #b6b8bb">
        <div style="padding-top: 32%">#f6f8fa</div>
</div>

## Fontes

A fonte utilizada para escrever qualquer coisa na tela do GitHub deve ser sempre a que vem por padrão nos styles da página.

Já a cor deve ser decidida em relação ao contexto, mas ainda respeitando a identididade visual do GitHub.

### Títulos

Os títulos de elementos, como gráficos por exemplo, devem ser `h2` e seguir a classe `"Subhead-heading"`, já definida na folha de estilo do GitHub. Alguns títulos devem ficar alinhados à esquerda, outros devem ficar ao centro da seção. Consulte protótipo.

### Números Grandes

Números que mereçam destaque, como os das barras de progresso definidas em protótipo, devem ser da tag `p` e da classe `"Subhead-heading"`, já definida na folha de estilo do GitHub.

### Textos Descritivos

Para pequenos textos de descrição, deve se utilizar a tag `spam` com a classe `"text-emphasized"` já definida na folha de estilo do GitHub.

### Demais Textos

Textos dentro de tabelas ou outros elementos que estejam densos devem seguir a tag `p`. O estilo padrão desse elemento no GitHub já é suficiente.

<br>