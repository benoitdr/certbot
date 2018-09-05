# certbot
Minimalistic docker container for certbot  
See https://letsencrypt.org/  
Build (for arm64) : https://hub.docker.com/r/benoitdr/certbot/

## Usage :  
### Get the certificate on first run :  
edit ./cert_get.sh (replace email and domain name)  
edit ./nginx/default.conf (replace domain name)  
```
cp docker-compose.yml_1 ./docker-compose.yml  
docker-compose up -d  
./cert_get.sh
docker-compose down  
cp docker-compose.yml_2 ./docker-compose.yml  
```

### Next run(s) :  
```
docker-compose up -d  
```

### To renew the certificate (in crontab) :  
```
./cert_renew.sh  
```
