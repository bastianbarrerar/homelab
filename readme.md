# nginx

localhost:81
default user and pass
admin@example.com:changeme

config inspiration https://notthebe.ee/blog/easy-ssl-in-homelab-dns01/

# nextcloud

(nginx) http://nextcloud:80 forceSSL HTTP/2 support

# onlyoffice

(nginx) https:onlyoffice:443 forceSSL HTTP/2 support

https://helpcenter.onlyoffice.com/installation/docs-community-install-docker.aspx

get secret for every docker-compose up down (nextcloud ONLYOFFICE secret key)

`docker exec <onlyoffice container ID> /var/www/onlyoffice/documentserver/npm/json -f /etc/onlyoffice/documentserver/local.json 'services.CoAuthoring.secret.session.string'`
