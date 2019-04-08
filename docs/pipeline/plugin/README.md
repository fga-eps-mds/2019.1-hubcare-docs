# Pipeline do plugin de chrome

![pipeline](pipelineplugin.png)

## Explicação sobre os estágios:

* **teste:** testes de unidade executam e publicam cobertura de teste no coveralls;
* **release:** gera uma compilação do aplicativo e publica na chrome store, são gerados apenas no branch master e devel; 
