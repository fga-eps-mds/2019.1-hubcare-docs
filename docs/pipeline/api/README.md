# Pipeline da api

<iframe frameborder="0" style="width:100%;height:446px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=pipeline%20api#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1-o7GaZhNaWqOITV1ssE8NWxC55tr1YjJ%26export%3Ddownload"></iframe>

## Explicação sobre os estágios:

* **teste:** São executados testes unitários do python e é publicada a cobertura do código no coveralls. Também é verificada a folha de estilo utilizando pep8; 
* **release:** Gera uma build do aplicativo utilizando o docker e em seguida a imagem é publicada no gitlab register, são gerados apenas nas branchs master e devel; 
* **deploy**: Atualiza a versão do sistema no deploy, são gerados apenas no branch master e devel. O deploy de produção é realizado no DigitalOcean utilizando o Rancher para gerenciar todos os serviços, já o deploy de homologação, que é realizado na devel, está configurado no Heroku utilizando o register do próprio  Heroku para atualizar o deploy.

## Ferramentas

### Gitlab CI/CD

O GitLab CI/CD é a ferramenta integrada do GitLab para desenvolvimento de software usando metodologia contínua:

* A Integração Contínua , ou CI, trabalha para integrar o código de sua equipe em um repositório compartilhado. Os desenvolvedores compartilham seu novo código em uma solicitação de mesclagem (pull), que aciona um pipeline para criar, testar e validar o novo código antes de mesclar as alterações em seu repositório.
* A Entrega Contínua , ou CD, entrega o código validado pelo CI para o seu aplicativo.

### Docker

Docker é uma ferramenta que permite que desenvolvedores, administradores de sistema, etc. implantem facilmente seus aplicativos em uma sandbox (chamados containers) para serem executados no sistema operacional host, ou seja, no Linux. O principal benefício do Docker é que ele permite que os usuários empacotem um aplicativo com todas as suas dependências em uma unidade padronizada para desenvolvimento de software. Ao contrário das máquinas virtuais, os contêineres não têm a alta sobrecarga e, portanto, permitem um uso mais eficiente do sistema e dos recursos subjacentes.

### Gitlab register

O Gitlab register é a ferrameta utilizada para criar, gerenciar e entregar os aplicativos de contêiner do projeto.

### Coveralls

Auxilia você a fornecer o código com segurança, mostrando quais partes do seu código não são cobertas pelo seu conjunto de testes.

### Rancher

É uma uma plataforma opensource para gerenciar infraestrutura de Docker e Kubernetes em produção, assim como efetuar deploy de apps usando Docker. O deploy é realizado em um server remoto na Digital Ocean. Ele é responsável por administrar e monitorar containers Docker.
