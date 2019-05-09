<div style="display: flex;">
<img src="https://upload.wikimedia.org/wikipedia/commons/4/4e/Docker_%28container_engine%29_logo.svg" height="64px"/>
<img src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Android_Emoji_2795.svg" height="64px">
<img src="https://upload.wikimedia.org/wikipedia/commons/3/34/Wordpress-logo-hoz-rgb.png" height="64px">
</div>


Boilerplate with Docker Compose files for WordPress in two different environments:
- local development with
    - adminer
- production environment with 
    - [nginx-proxy](https://github.com/jwilder/nginx-proxy)
    - [letsencrypt-nginx-proxy-companion](https://github.com/JrCs/docker-letsencrypt-nginx-proxy-companion). It uses different docker compose config files for each environment.

# Quick start
```bash
git clone git@github.com:5queezer/docker-wordpress.git
cd docker-wordpress
docker-compose up -d
```

# Add a theme from Git
```bash
git submodule add git@github.com:WordPress/twentynineteen.git themes/twentynineteen
```

Uncomment theme entry volume from `docker-compose.yml` and edit the theme folder name (2x).

# Plugins
Proceed in a similar manner as for the themes in the section above.
