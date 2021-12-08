# Sobre o ICAM

Este projeto foi desenvolvido em 2019 (1ª onda covid19 em portugal) por uma equipa de voluntários dentro do movimento #tech4covid19 em colaboração com pessoal do Centro Biomédico do Algarve de acordo com situação descrita abaixo:

- **Factos:**  
  Todos os dias são publicados artigos científicos com nova informação sobre o coronavírus que pode fazer a diferença para os profissionais.
- **Problema:**  
  Os médicos queixam-se da dificuldade de recolher e rever toda a informação à procura de algo que lhes seja relevante.
- **Solução:**  
  Plataforma online que:  
  Recolhe artigos de repositórios específicos  
  Revisores selecionam artigos relevantes e escrevem sinopses em português.  
  Acesso público às sinopses.  

Atualmente o projeto encontra-se morto (site offline) e estes repositórios servem apenas de registo histórico caso alguém tenha interesse em aproveitar código / ideias.

# Execução da plataforma em dev

clone application/registry

    https://github.com/ABC-COVID19/API-registry.git

clone application/microservice

    https://github.com/ABC-COVID19/API-backend.git
    
clone application/gateway

    https://github.com/ABC-COVID19/API-backoffice.git

before build

    prepare environment after reading each repository README.md

build application/registry

    ./mvnw
    
build application/microservice

    ./mvnw
    
build application/gateway

    ./mvnw
    
URL: http://localhost:8080
Username: admin
Password: admin
    
# Recriação da plataforma (backend + backoffice)

create application/microservice

    recepie-api.png

create application/gateway

    recepie-backoffice.png

microservice
    
    jhipster import-jdl '../backend/model/jhipster-jdl-v1.jh' --force

gateway (valid for develop branch. Master is behind)

    jhipster entity ArticleType --force
    jhipster entity CategoryTree --force
    jhipster entity SourceRepo --force
    jhipster entity Revision --force
    jhipster entity Article --force
    jhipster entity Newsletter --force
    
