# Sobre o Projeto

Como é fácil e rápido trabalhar com laravel do jeito certo, entendendo como o framework funciona e a encaixar cada peça para desenvolver projetos profissionais, seguros, escaláveis e de alto valor no menor tempo possível
- <a href="https://www.youtube.com/playlist?list=PLi_gvjv-JgXqop7hgVKZMGPiT9rUYy1srs">LARAVEL TIPS</a> - Gustavo Web


## Requerimentos

- Install <a href="https://docs.docker.com/install/">Docker</a>

- Install <a href="https://docs.docker.com/compose/install/">docker-compose</a>

- PHP >= 7.1

- Postgres >= 9.4 ou Mysql >= 5.7


## Instalação
Realizar o git clone do projeto
```bash
git@github.com:viniciusmattosrj/laravel-tips.git
```

Para que o git não considere alterações de permissão como modificações a serem rastreadas, execute:
```
git config core.fileMode false
```

Entre pelo terminal na pasta do projeto e rode:
```
cp ./docker-compose-example.php  ./docker-compose.php
```

Agora suba o servidor:
```
docker-compose up -d
```

Em outra aba do terminal se conecte no container do php e inicie um servidor built in do PHP
```
docker exec -it php bash
php -S 10.11.0.11:8008 -t public
```

No browser digite http://10.11.0.11:8008

Criando banco dados postgres: 

```
docker exec -it postgres bash
psql -U webadm -c "CREATE DATABASE laravel_tips";
```

Realizando a importação dump sql para a base criada:
```
psql -U webadm php_ajax < /var/lib/postgresql/sqlscript/laravel_tips.pgsql
```

Para o acesso no <strong>POSTGRES</strong> database administration tool, use http://localhost:5050 e use as credênciais abaixo:

  - server:
  - username:
  - password:


Criando banco dados postgres: 

```
docker exec -it mysql bash
mysql -u root -c "CREATE DATABASE laravel_tips;"
```

Realizando a importação dump sql para a base criada:
```
mysql -u root -p laravel_tips < /var/lib/mysql57/laravel_tips.sql
```

Para o acesso no <strong>MYSQL</strong> database administration tool, use http://localhost:8080 e use as credênciais abaixo:

  - server:
  - username:
  - password:


## Contribuições
Caso identifique pontos
que possam ser aprimorados envie o seu PR. ;-)


## License
[MIT](https://choosealicense.com/licenses/mit/)
