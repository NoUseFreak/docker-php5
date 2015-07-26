FROM debian:squeeze

RUN apt-get update \
	&& apt-get install -y php5

COPY apache.conf /etc/apache2/apache.conf
COPY apache-vhost.conf /etc/apache2/sites-enabled/000-default

COPY apache2-foreground /usr/local/bin/
WORKDIR /var/www/html

EXPOSE 80
CMD ["apache2-foreground"]
