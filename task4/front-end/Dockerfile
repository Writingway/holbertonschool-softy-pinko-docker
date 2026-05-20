FROM nginx:latest

# Copier le contenu du dossier softy-pinko-front-end directement (pas le dossier lui-même)
COPY softy-pinko-front-end/ /var/www/html/softy-pinko-front-end/

# Copier la config nginx
COPY softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf

EXPOSE 9000