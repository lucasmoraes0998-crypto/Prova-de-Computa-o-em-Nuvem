# Prova-1-de-Computacao-em-Nuvem

Nome: Lucas Alberto Ferraz de Toledo Moraes
RA: f7571f6670c2b3f75fda

## O que fiz:
Executei uma página web em um contêiner Docker chamado Estoque.
Usei a imagem nginx:alpine e a porta 8085 do ambiente.

## Verificaçãp dp contêiner:
root@ubuntu:~$ docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED              STATUS              PORTS                                     NAMES
98f249c6357c   nginx:alpine   "/docker-entrypoint.…"   About a minute ago   Up About a minute   0.0.0.0:8085->80/tcp, [::]:8085->80/tcp   estoque

## Teste da página:
root@ubuntu:~$ curl http://localhost:8085
<!DOCTYPE html>
<html lang="pt-BR">
<head>
 <meta charset="UTF-8">
 <title>Estoque</title>
</head>
<body>
 <h1>Estoque Disponivel</h1>
</body>
</html>

## Explicação 
A diferença é que nginx:alpine é a imagem usada como base para criar o contêiner, enquanto Estoque é o nome dado ao contêiner que foi criado a partir dessa imagem.

nginx:alpine → é a imagem do Nginx, uma versão mais leve baseada no Alpine Linux.
Estoque → é o contêiner em execução, criado usando essa imagem.

O mapeamento 8085:80 serviu para ligar a porta 8085 do computador à porta 80 do contêiner. Assim, quando você acessa localhost:8085, a requisição é direcionada para o Nginx dentro do contêiner, que está funcionando na porta 80.
