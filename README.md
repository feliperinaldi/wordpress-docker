# Wordpress-Docker Dev Environment
Wordpress-Docker development environment

Ensinado na live 53: [AprendaWP com Felipe Rinaldi](https://www.youtube.com/channel/UC-LKig8NJbVzDdTnEmRHVRQ/)

Entre para a lista de emails: [FelipeRinaldi.com](https://feliperinaldi.com)

Atalho para instalar diretamente um novo wordpress na máquina:
$ git clone git@github.com:feliperinaldi/wordpress-docker.git && cd wordpress-docker && docker-compose up -d

Para customizar cada nova instalação:
1. Primeiro clone o repositório e entre na pasta: 
$ git clone git@github.com:feliperinaldi/wordpress-docker.git && cd wordpress-docker

2. Depois edite o arquivo .env na linha 5: PROJECT_NAME - substituindo dockerwp pelo slug da sua aplicação.
Isso fará com que todos os containers dessa instalação tenha seu slug único no início.

3. Inicie os containers:
$ docker-compose up -d

Para usar o WP Cli:

O WP Cli desta instalação encontra-se no container do wordmove. Desta forma, após a instalação seguindo os passos anteriores, basta:

1. Na pasta da nova instalação (padrão wordpress-docker):
$ docker exec -it seu_slug_wordmove /bin/bash

2. Dentro do bash, vá para o Container do WP e seja feliz:
$ cd /var/www/html && wp --version --allow-root
Note: ao final do comando, sempre use --allow-root para que seu comando do wp cli possa ser executado.