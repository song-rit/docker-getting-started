FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
	htop \
	vim \
	nano \
	curl \
	apache2 \ 
	php5

COPY /apache2 /etc/apache2
COPY /web /var/www/html/web

EXPOSE 80
CMD ["echo", "Hello This is basic apache2 && php5"]
CMD echo "Please restart apache2"
CMD apachectl -DFOREGROUND
