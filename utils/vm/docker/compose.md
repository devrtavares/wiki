# docker

<sub>[:arrow_upper_left: docker](readme.md)<sub>

## comando : compose

Docker-compose é um comando que busca um arquivo no diretório de invocação, para através dele gerenciar uma imagem de sistema, criando, fazendo download, executando e configurando.

- Chamada do comando: 
```
docker-compose up -d
```

- Exmeplo de arquivo de composição:
```json
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
```