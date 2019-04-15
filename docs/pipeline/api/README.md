# Pipeline da api

<iframe frameborder="0" style="width:100%;height:446px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=pipeline%20api#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1-o7GaZhNaWqOITV1ssE8NWxC55tr1YjJ%26export%3Ddownload"></iframe>

## Explicação sobre os estágios:

* **teste:** testes de unidade executam e publicam cobertura de teste no coveralls; 
* **release:** gera uma build do aplicativo e publica no dockerhub, são gerados apenas no branch master e devel; 
* **deploy**: atualiza a versão do sistema no deploy, são gerados apenas no branch master e devel (em desenvolvimento)