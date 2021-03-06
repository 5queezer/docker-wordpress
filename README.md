# Wordpress Docker
Wordpress Docker with [Nginx-Proxy](https://hub.docker.com/r/jwilder/nginx-proxy) with the [Letsencrypt integration](https://hub.docker.com/r/jrcs/letsencrypt-nginx-proxy-companion/).

<div style="display: flex;">
<img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Docker_%28container_engine%29_logo.svg" height="64px"/>
<img src="https://upload.wikimedia.org/wikipedia/commons/9/9e/Plus_symbol.svg" height="64px">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Wordpress-logo-hoz-rgb.png" height="64px">
</div>

This is a boilerplate with Docker Compose files for WordPress in two different environments:
- local development with
    - [adminer](https://hub.docker.com/_/adminer/)
- production environment with 
    - [nginx-proxy](https://github.com/jwilder/nginx-proxy)
    - [letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion).

# Quick start
## Installation
```bash
git clone git@github.com:5queezer/docker-wordpress.git
cd docker-wordpress
```

## Development environment
```bash
docker-compose up -d
```
Open your browser at [http://localhost](http://localhost). The adminer is located at [http://localhost:8080](http://localhost:8080)

## Production environment
For production the **.env** file is necessary. Copy the sample file and modifiy the values. 
```bash
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d
```

# Wordpress Credentials
Use the Bitnami credentials. Username _user_, Passwort _bitnami_

# Themes
Add a theme from git as submodule:
```bash
git submodule add git@github.com:WordPress/twentynineteen.git themes/twentynineteen
```

Uncomment theme entry volume from `docker-compose.yml` and edit the theme folder name (2x).

## Plugins
Proceed in a similar manner as for the themes in the section above.
