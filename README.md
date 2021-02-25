[Iniciando novo projeto laravel com docker](https://github.com/thiagotrancoso/docker/wiki/Iniciando-novo-projeto-laravel-com-docker)

> **OBS**: ESTA ESTRUTURA DO DOCKER FOI PENSADA PARA PROJETOS COM O LARAVEL

# Estrutura base para novos projetos com Docker

Clone o repositório com a estrutura do docker
```bash
git clone git@github.com:thiagotrancoso/docker.git
```

Altere o nome da pasta para o nome do projeto
```bash
mv docker nome_projeto
```

Remova a pasta `.git` e  o arquivo `README.md`
```bash
cd nome_projeto
sudo rm -rf .git README.md
```

> Coloque os arquivos do projeto dentro da pasta `/meu_projeto/www`.

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

# Outras configurações
### Se alterar o nome do container do PHP altere também no arquivo `default.conf`

```json
// O "php" na linha de baixo é o nome do container
fastcgi_pass php:9000;
```
