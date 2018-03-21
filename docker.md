# Hello, Docker
[imagem da baleia]
- Docker -> Containers Linux[?]
- Container
    - Encapsula minha aplicação
    - Tipo uma VM?



# Container vs VM
- Spoiler: É mais leve
    - [imagem comparando VM e Container]



# Por que VMs (ou containers)?
- ~~custo~~
- [etc]
- **automação!**
    - "Infrastructure as Code"



# 12 factor apps
[]



# DevOps
[ ...  ]
- Não dá mais para tratar infra como caixa preta.
  - De fato, nunca foi...
  - `appsrv-a`, `appsrv-b`, `unificadorpdf-a`, `unificadorpdf-b`



# Docker, ferramenta
- Fachada para alguns componentes do Linux:
  - `namespaces` (isola visibilidade processos)
  - `cgroups` (restringe recursos usado por processos)
  - `iptables` (restringe acesso a interfaces de rede)
- cli & api



# `docker`
[  ] Instalar o toolbox no desktop do tribunal e executar as práticas



## Imagens
- dockerhub
- rootfs
  - imagens têm camadas
  - cada camada é como um commit do git
  - imagens derivadas de uma imagem comum compartilham camadas



## Criando meu primeiro container
- docker run centos:7 --name meucentos
- docker exec meucentos
- attached vs dettached
  - ps aux
- --rm
- docker stats
- docker top



## Executando algum serviço
- Portas
- docker logs
- docker commit



## Infra como código, você disse...



### Dockerfile
    [mostrar a jurisprudencia como exemplo]



### docker-compose



# Como adotar, gradualmente



## Desenvolvimento
- Servidor de aplicação, identico a produção
- Testar tecnologias novas (já tentou Java 10?)
- Mais de uma instância rodando, ao mesmo tempo.



## CI / CD
- Testes / Homologação
  - Diferentes branches, executando ao mesmo tempo
      [  ] Estudar como funciona o CI do gitlab



## Isolar aplicações de terceiros
- folha web (wildfly 8)
- otrs (apache + perl)
- sigeo (jboss 5)
- scmp (jboss 4)



## Isolar aplicações complexas (várias partes móveis)
- unificadorpdf
- plone
- jurisprudencia



## Isolar ambientes críticos
- `apprsrv-a` e `appsrv-b`
- `unificadorpdf-a` e `unificadorpdf-b`
- `transparencia-a` e `transparencia-b`



# Subindo o nível: Kubernetes
- Gerencia clusters
 -
[  ]
