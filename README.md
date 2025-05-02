# Gerenciamento de Contatos

## Executar os comandos abaixo para executar o projeto:

### Clonar o Repositório
```sh
git clone git@github.com:andrescherrer/contatos-uex.git contatos
```
### Acessar a pasta do projeto
```sh
cd contatos
```
### Criar o .env a partir .env.example
```sh
cp .env.example .env
```
### Fazer build das imagens e subir os containers
```sh
docker compose up --build -d
```
### Consultar o IP do container do MySQL
```sh
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' contatos-db
```
### Substituir na chave DB_HOST do .env
```sh
copiar o ip do comando anterior e substituir em DB_HOST= no .env
```
### Acessar o container contatos-app
```sh
docker exec -it contatos-app bash
```
### Instalar as dependências do projeto
```sh
composer install
```
### Rodar as migrações
```sh
php artisan migrate
```
