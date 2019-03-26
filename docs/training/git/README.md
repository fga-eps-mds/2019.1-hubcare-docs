# Treinamento de Git

**Resposáveis**: [Cleber Castro](https://github.com/cjjcastro)

**Data**: 19/03/2019

**Membros do Time que Compareceram**: [Francisco](https://github.com/FranciscoHeronildo), [Vitor Alves](https://github.com/vitorAlves7), [Vitor Meireles](https://github.com/VitorMeirelesOliveira), [Brian Lui](https://github.com/Brian2397), [Jacó Apolinário](https://github.com/Jacoapolinario)

## Contexto

Visando preparar a equipe de desenvolvimento pra a execução do projeto, preparamos um treinamento sobre git para garantir o conhecimento da equipe sobre o mesmo.

## Formato do Treinamento

Para melhor compreensão dos participantes do treinameto criamos um repositório para executar os comandos ao mesmo tempo que cada um era explicado.

## Material Utilizado

A seguir estão os comandos apresentados e uma breve descrição de cada.

### Git
_____

#### Iniciar um projeto
Para iniciar  o git no seu projeto utilize o comando:
> git init

#### Obter um repositório
Para criar uma cópia de um trabalho em repositório remoto
> git clone usuário@servidor:/caminho/para/o/repositório

#### Adicionar arquivos alterados
> git add <arquivo>

Para inserir todos os arquivos modificados
> git add *


#### Confirmar mudanças

> git commit -m "comentario"

> git commit -s

##### inserir Co-authored-by
> Co-authored-by: another-name <another-name@example.com>"

#### Enviando alterações
> git push origin <branch>

#### Inserindo repositórorio remoto
> git remote add origin <path>

#### Ramificando
##### Para criar uma nova branch
> git checkout -b <branch_name>

##### Para alterar de branch
> git checkout <branch_name>

##### Para remover uma branch (LOCAL)
> git branch -d <branch_name>

#### Atualizar repositório local
> git pull

> git pull origin <branch_name>

#### Visualizar diferenças entre branch
> Git diff <branch1> <branch2>

#### Visualizar commits
> git log

#### Sobrescrever alterações locais
> git checkout -- <file>

#### Remover todas alterações locais
> git stash

