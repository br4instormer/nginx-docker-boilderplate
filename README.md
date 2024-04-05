# nginx-docker-boilerplate

Blueprints to quick deployment web app within Docker using Nginx as reverse proxy

## Install certbot and certificates

```bash
sudo snap install core; sudo snap refresh core
sudo apt remove certbot
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot

mkdir -p ./letsencrypt/sitename.zone/.well-known

certbot certonly --email email@example.com --webroot -w ./letsencrypt/sitename.zone -d sitename.zone
```
