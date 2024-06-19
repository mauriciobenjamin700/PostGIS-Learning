# Repositório destinado ao aprendizado do uso da extensão PostGIS do PostgreSQL

Saudações pessoal, este "projeto" visa ajudar nos primeiros passos sobre o uso do PostGIS

## O que é o PostGIS?

O PostGIS é uma extensão espacial gratuita e de código fonte livre. Sua construção é feita sobre o sistema de gerenciamento de banco de dados objeto relacional PostgreSQL, que permite o uso de objetos GIS ser armazenado em banco de dados. 

[Clique aqui para ver Documentação Oficial](https://postgis.net/)

## Dependências de Sistema

Sou um usuário windows, portanto estarei usando a ferramenta [WSL](https://learn.microsoft.com/pt-br/windows/wsl/) para usar um subsistema linux no meu windows. Para este caso estarei usando o [Linux Ubuntu 22.04 LTS](https://ubuntu.com/blog/tag/22-04-lts).

Caso você seja usuário linux, creio que os passos a baixo vão servir da mesma forma.

## Ferramentas de Apoio

Para não precisar instalar nada diretamente no meu sistema, irei usar o [docker](https://www.docker.com/) para garantir que tudo será replicavel atráves dos conteiners

## Instalações

Tendo o WSL e Docker Instalados, vamos para os conteiners que iremos usar

## PostgreSQL

Já deixei configurado arquivo [docker-compose](docker-compose.yaml) para usamos.

- Suba a instancia do Banco usando `docker-compose up --build -d`
- Conecte-se ao banco usando PGadmin ou Dbeaver com as seguintes credenciais de acesso:
  - host: localhost
  - database: `postgres`
  - port: `1234`
  - user: postgres
  - password: postgres

Caso o postgis ainda assim não esteja ligado, abra um terminal SQL pelo dbeaver e execute a seguinte Query `CREATE EXTENSION postgis`

Para desligar o conteiner use `docker-compose down`


## Opções de Serviços para Hospedagem Postgres + PostGIS

- [supabase](https://supabase.com/pricing)
- [heroku](https://devcenter.heroku.com/articles/heroku-postgresql)