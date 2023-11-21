FROM ubuntu

RUN apt update && \
echo "y" | apt install nginx

RUN mkdir -p /var/www/html/marmotte.fr && \
echo "Bonjour depuis un dockerfile" >> /var/www/html/marmotte.fr/index.html

Run usermod -u 1000 www-data


COPY marmotte.conf /etc/nginx/sites-enabled/

CMD ["nginx", "-g", "daemon off;"]
