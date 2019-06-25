# Pipeline do plugin de chrome

**Autor: Cleber Castro**

<iframe frameborder="0" style="width:100%;height:516px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=pipeline%20plugin#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1MIYlyS-hRLhXL6E_QW0VN7YmHnUUDcga%26export%3Ddownload"></iframe>

## Explicação sobre os estágios:

* **test:** Testes unitários são exucutados utilizando jest-js e é publicada a cobertura do código no codecov;
* **release:** Gera uma build do aplicativo utilizando o docker e em seguida a imagem é publicada no gitlab register, apenas na branch master esse processo é executado. São geradas releases para homologação e para produção, no primeiro caso todo código que for para a branch master executa o processo de release, já as releases de produção são geradas a partir de Tags/Releases do Github;
* **publish:** Gera uma build do aplicativo e é publicada na chrome store utilizando a api do google, apenas na branch master esse processo é executado. São publicados para homologação e para produção, no primeiro caso todo código que for para a branch master executa o processo de publicação, já e, produção são publicadas a partir de Tags/Releases do Github;

## Ferramentas

### Gitlab CI/CD

O GitLab CI/CD é a ferramenta integrada do GitLab para desenvolvimento de software usando metodologia contínua:

* A Integração Contínua , ou CI, trabalha para integrar o código de sua equipe em um repositório compartilhado. Os desenvolvedores compartilham seu novo código em uma solicitação de mesclagem (pull), que aciona um pipeline para criar, testar e validar o novo código antes de mesclar as alterações em seu repositório.
* A Entrega Contínua , ou CD, entrega o código validado pelo CI para o seu aplicativo.

### Gitlab register

O Gitlab register é a ferrameta utilizada para criar, gerenciar e entregar os aplicativos de contêiner do projeto.

### Codecov

Auxilia você a fornecer o código com segurança, mostrando quais partes do seu código não são cobertas pelo seu conjunto de testes.
