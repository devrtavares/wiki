# postgresql

<sub>[:arrow_upper_left: postgresql](readme.md)</sub>

## instalação

### 1. **Docker compose**

- requisitos
    - *docker desktop*
    - *visual studio code*

- Exemplo para windows:

    vamos criar um diretório e um arquivo através do therminal
    ```
    cd /d Desktop
    mkdir env-postgreesql-dev-start
    code docker-compose.yml
    ```
    ...salve o arquivo "[docker-compose.yml](docker-compose.yml)" com o conteúdo: 

    ```
    version: '3'

    services:
        db-postres-dev:
            image: postgres
            environment:
                POSTGRES_PASSWORD: "12345"
            ports:
                - "5432:5432"
            volumes:
                - /home/mycomputer/desenvolvimento/docker-Compose/postgresql:/var/lib/postgresql/data
            networks:
                - db-postres-dev-network
            driver: bridge
    ```
    ...executando o composer:
    ```
    docker-compose up -d
    ```
    ...validando a conexão gerada:
    ```
    docker network ls
    ```

[*referência*](https://renatogroffe.medium.com/postgresql-pgadmin-4-docker-compose-montando-rapidamente-um-ambiente-para-uso-55a2ab230b89)

<sup></sup>
---

#### Extras:
- [*Extensão docker para visual studio code*](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker)

