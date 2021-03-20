## Tutoriais
* [Iniciando novo projeto laravel com docker](https://github.com/thiagotrancoso/docker/wiki/Iniciando-novo-projeto-laravel-com-docker)
* [Configurando url personalizada em ambiente local](https://github.com/thiagotrancoso/docker/wiki/Configurando-url-personalizada)

## Containers
> Caso queira uma versão diferente do `PHP`, altere o arquivo `docker/php/Dockerfile`.  
> Caso queira uma versão diferente de outro serviço, altere o arquivo `docker-compose.yml`.

* PHP 7.4-fpm
* Nginx 1.19
* MariaDB 10.5
* PhpMyAdmin 5.1

## Outras configurações
### Se alterar o nome do container do PHP altere também no arquivo `default.conf`

```json
# O "php" na linha de baixo é o nome do container
fastcgi_pass php:9000;
```
