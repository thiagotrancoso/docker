[Iniciando novo projeto laravel com docker](https://github.com/thiagotrancoso/docker/wiki/Iniciando-novo-projeto-laravel-com-docker)

# Outras configurações
### Se alterar o nome do container do PHP altere também no arquivo `default.conf`

```json
# O "php" na linha de baixo é o nome do container
fastcgi_pass php:9000;
```
