# certbot-docker
certbotのDockerコンテナを用いてLet's Encryptから証明書を取得する。

## Usage
standalone  
 ```bash
 DOMAIN=example.com \
 EMAIL='user@example.com' \
 docker-compose run --rm --service-ports standalone
 ```
webroot
 ```bash
DOMAIN=example.com \
EMAIL='user@example.com' \
WEBROOTPATH='/var/www/certbot' \
docker-compose run --rm webroot
 ```
renew
```bash
docker-compose run --name certbot_renew renew
```

## Requirement
Domain  
Docker,docker-compose
