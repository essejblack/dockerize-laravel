# Laravel Docker
Configs for mysql , laravel , nginx to dockerize project , Dockerfile - docker compose 

Docker Compose Version : 3.8

## Services
- mysql
- php 8.1-fpm
- nginx
- phpmyadmin 5

### Essential Packages
- make
- docker

### DB Config

you need to change in env file :
- DB_DATABASE
- DB_PASSWORD

by your docker-compose file

### Nginx

some of configs need to be fixed and update
server_name it's not usable

#### Usage

- change ports , service names if needed

after installing essential packages :

1. `make build`
it's same as `docker compose build`
2. `make up`
it's same as `docker compose up -d`

if you have change configs you need
`make down`
then
`make up`

if you have change "app.dockerfile"
for example adding some packages or changing versions you need to :

1. `make down`
2. `make build`
3. `make up`

however using `make` commands are not necessary you could use `docker compose` commands.

Good Luck.