# Nginx

access localhost:81

default user and pass

admin@example.com:changeme

config inspiration https://notthebe.ee/blog/easy-ssl-in-homelab-dns01/

# Nextcloud

- Nginx Config

http://nextcloud:80 _forceSSL HTTP/2 support_

- Add cron job to host

```bash
crontab -e
```

paste at the end

```bash
*/5 * * * * docker exec -i -u www-data <nextcloud container ID> php -f /var/www/html/cron.php
```

# Onlyoffice

- Nginx Config

https://onlyoffice:443 _forceSSL HTTP/2 support_

- Onlyoffice Guide

https://helpcenter.onlyoffice.com/installation/docs-community-install-docker.aspx

get secret for every docker-compose up down (nextcloud ONLYOFFICE secret key)

```bash
docker exec <onlyoffice container ID> /var/www/onlyoffice/documentserver/npm/json -f /etc/onlyoffice/documentserver/local.json 'services.CoAuthoring.secret.session.string'
```
