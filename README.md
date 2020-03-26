# docs
Repositório para centralização de documentação

# Execução da plataforma em dev

clone application/registry

    https://github.com/ABC-COVID19/API-registry.git

clone application/microservice

    https://github.com/ABC-COVID19/API-backend.git
    
clone application/gateway

    https://github.com/ABC-COVID19/API-backoffice.git
    
build application/registry

    ./mvnw
    
build application/microservice

    ./mvnw
    
build application/gateway

    ./mvnw
    
aceder a http://localhost:8080
    
# Recriação da plataforma (backend + backoffice)

create application/microservice

    recepie-api.png

create application/gateway

    recepie-backoffice.png

microservice
    
    jhipster import-jdl '../backend/model/jhipster-jdl-v1.jh' --force

gateway

    jhipster entity ArticleType --force
    jhipster entity CategoryTree --force
    jhipster entity PublicationSource --force
    jhipster entity Article --force
    jhipster entity Revision --force
    jhipster entity Newsletter --force
