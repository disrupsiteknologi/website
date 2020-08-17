FROM php:7.4-apache

COPY etc /etc

RUN apt update -y && \
    apt install certbot python3-certbot-apache -y && \
    a2enmod rewrite && \
    a2dissite 000-default && \
    a2ensite disrupsiteknologi.com && \
    a2ensite disrupsiteknologi.com-ssl && \
    a2ensite disrupsiteknologi.com-dir && \
    service apache2 restart

EXPOSE 80
EXPOSE 443