# Pipeline do plugin de chrome

<iframe frameborder="0" style="width:100%;height:516px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=pipeline%20plugin#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1MIYlyS-hRLhXL6E_QW0VN7YmHnUUDcga%26export%3Ddownload"></iframe>

## Explicação sobre os estágios:

* **teste:** Testes unitários são exucutados utikizando jest-js e é publicada a cobertura do código no coveralls;
* **release:** Gera uma build do aplicativo utilizando o docker e em seguida a imagem é publicada no dockerhub, são gerados apenas nas branchs master e devel; 
* **release:** Gera uma build do aplicativo e é publicada na chrome store utilizando a api do google, são gerados apenas no branch master e devel; 

## Ferramentas

### Gitlab CI/CD

O GitLab CI/CD é a ferramenta integrada do GitLab para desenvolvimento de software usando metodologia contínua:

* A Integração Contínua , ou CI, trabalha para integrar o código de sua equipe em um repositório compartilhado. Os desenvolvedores compartilham seu novo código em uma solicitação de mesclagem (pull), que aciona um pipeline para criar, testar e validar o novo código antes de mesclar as alterações em seu repositório.
* A Entrega Contínua , ou CD, entrega o código validado pelo CI para o seu aplicativo.

### DockerHub

O Docker Hub é a ferrameta utilizada para criar, gerenciar e entregar os aplicativos de contêiner do projeto.

### Coveralls

Auxilia você a fornecer o código com segurança, mostrando quais partes do seu código não são cobertas pelo seu conjunto de testes.
