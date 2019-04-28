
### GitFlow

#### Política de Commits

Os commits devem ser significativos e feitos de forma sucinta descrevendo o que foi feito, portanto o commit deve ser atômico descrevendo a funcionalidade que foi implementada.

E caso exista necessidade comentar com mais detalhes o que foi implementado e o motivo.

Exemplo - "Create new class for user"

### Política de Branches

O repositório do projeto possui duas branches principais para o desenvolvimento: master e devel, e as branches auxiliares contendo as funcionalidades desenvolvidas.

A branch master conterá a versão estável, o seu conteúdo será proveniente da branch de desenvolvimento (devel) após a aprovação do pull request. 

A branch devel será utilizada para o desenvolvimento, onde a integração das funcionalidades desenvolvidas pela equipe nas branches auxiliares ocorrerá.

As branches auxiliares serão utilizadas para o desenvolvimento das funcionalidades.Essas branches serão nomeadas de acordo com a issue qual ela é relacionada.

* Exemplo : "feature-create_new_user".

Os bugs seguirão o formato padrão no projeto: bug-< Nome do bug> e dentro dele uma descrição do problema e se necessário o fluxo que levou até o bug.

* Exemplo : "bug-login".

### Política de Aprovação do Código

O nome do __pull request__ será o nome da issue sendo feito de sua branch para a devel.

O __PO__ é o responsável de avaliar os __PRs__ se eles cumprem com os requisitos descritos e se ele segue a folha de estilo proposta.

### Uso de Issues

As issues do github serão usadas para se ter um maior controle sobre o que se é desenvolvido as issues representarão as histórias de usuário. 

Será cadastrada as tasks e os critérios de aceitação de cada história de usuário seguindo o __template__ definido, além dessa ser especificada em voz de usuário. A especificação da história de usuário seguirá o seguinte padrão: Eu, como <usuário> desejo <meta/desejo>, para <benefício>.

* Exemplo: “Eu, como gerente, desejo cadastrar novos produtos, para manter meu estoque sempre atualizado.”

O nome das issues seguirão o seguinte padrão: <Tipo de Issue> - < Nome definido para a história pela equipe >.

* Exemplo : "Feature - Register Product".

<br>