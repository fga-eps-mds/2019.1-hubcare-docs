# Treinamento de Git

**Resposáveis**: [Cleber Castro](https://github.com/cjjcastro)

**Data**: 21/03/2019

**Membros do Time que Compareceram**: [Francisco](https://github.com/FranciscoHeronildo), [Vitor Alves](https://github.com/vitorAlves7), [Vitor Meireles](https://github.com/VitorMeirelesOliveira), [Brian Lui](https://github.com/Brian2397), [Jacó Apolinário](https://github.com/Jacoapolinario)

## Contexto

Para uma melhor compreensão da equipe sobre como o ambiente de desenvolvimento funcionará ao decorrer do semestre, foi aplicado um treinamento sobre docker. Docker é uma tecnologia de software que fornece contêineres, e será utilizada por facilitar a configuração do ambiente de desenvolvimento.

## Formato do Treinamento

A princpipio, foi apresentado através de slides os conceitos e comando básicos e uma breve explicação do que é docker e para que serve.
Em seguida, foi apresentado na prática o funcionamento do docker.

## Material Utilizado

Material de apoio:

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRgLBDq1TzkXXyDw1iU_HdsBQlcOtcslj8GyeqVOGN37BPHOcPo9khCnsPFQm3HY89ROBTOM-oDUXZU/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="549" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

### Comando do docker

#### Comandos básicos

```bash
docker version # Verifica a versão do  Docker
docker image ls # Lista as imagens presentes no host
docker image inspect # Traz detalhes de determinada imagem
docker image rm image_name # Remove uma imagem
docker container run # Executa um container
docker container ls # Lista os containers em execução
docker container inspect # Traz detalhes de determinado container
docker container ls -a # Lista todos os containers, inclusive os parados
docker container stop # Para um container
docker container start # Inicia um container
docker container restart # Reinicia um container
docker container rm container_name # Remove um container
docker container rm container_name -f # Remove um container em execução
docker container top # Traz os processos em execução
docker container stats # Traz informações sobre o consumo de recursos como CPU e memória
docker container exec # Executa algo no container
docker container attach # Conecta no container
```
### Docker swarm

O swarm é uma ferramenta nativa de orquestração do docker. Ela permite que containers executem distribuídos em um cluster, controlando a quantidade de containers, registro, deploy e update de serviços.

Um swarm é um grupo de máquinas que executam o docker e se juntam a um cluster. Depois disso, você continuará executando os comandos do docker aos quais está acostumado, mas agora eles são executados em um cluster por um gerenciador swarm. As máquinas em um swarm podem ser físicas ou virtuais. Depois de se juntar a um swarm, eles são chamados de nodes.

#### Comandos swarm

```bash
docker swarm init # Inicia um cluster swarm
docker swarm join # Comando para adicionar novos nodes no cluster
docker node ls # Lista os nodes do cluster
docker swarm join-token manager # Lista o token para adicionar novos managers ao cluster
docker swarm join-token worker # Lista o token para adicionar novos workers ao cluster
docker node inspect # Traz detalhes sobre o node
docker node promote # Promove um node para manager
docker node demote # Muda um node para worker
docker node rm # Remove um node
docker swarm leave # Para que o node saia do cluster
docker swarm leave --force # Para que um node manager saia do cluster 
```

### Docker service

Em um aplicativo distribuído, diferentes partes do aplicativo são chamadas de "serviços". Por exemplo, se você imaginar um site de compartilhamento de vídeo, ele provavelmente inclui um serviço para armazenar dados do aplicativo em um banco de dados, um serviço para transcodificação de vídeo em segundo plano depois que um usuário fizer upload de algo, um serviço para o front-end e assim por diante.

Os serviços são realmente apenas "contêineres em produção". Um serviço só executa uma imagem, mas codifica a maneira como a imagem é executada - que portas devem ser usadas, quantas réplicas do contêiner devem ser executadas para que o serviço tenha a capacidade necessária e em breve. O dimensionamento de um serviço altera o número de instâncias de contêiner que executam esse software, atribuindo mais recursos de computação ao serviço no processo.

Felizmente, é muito fácil definir, executar e dimensionar serviços com a plataforma Docker. Basta escrever um arquivo ```docker-compose.yml```.

#### Comandos service

```bash
docker service create # Cria um serviço
docker service ls # Lista os serviços
docker service inspect # Traz detalhes sobre o service
docker service scale # Aumenta/Diminui a quantidade de réplicas de um service
docker service ps # Lista os pods de um service
docker service logs # Traz os logs de um service
docker service rm # Remove um service
```

### Docker stack

Um stack é um grupo de serviços inter-relacionados que compartilham dependências e podem ser orquestrados e escalonados juntos. Um único stack é capaz de definir e coordenar a funcionalidade de um aplicativo inteiro.

#### Comandos stack

```bash
docker stack deploy # Realiza o deploy de uma stack
docker stack ls # Lista as stacks
docker stack services # Lista os services de uma stack
docker stack rm # Remove uma stack
docker stack inspect # Traz detalhes sobre uma stack
```
