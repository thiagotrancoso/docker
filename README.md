# Estrutura base para novos projetos com Docker

# Antes de iniciar os containers

Vá no arquivo `docker-compose.yml` e altere o argumento `user`.

```yml
services:
  php:
    build:
      args:
        uid: 1000
        user: thiago    # Altere o nome "thiago" para o nome de usuário da máquina host
```
