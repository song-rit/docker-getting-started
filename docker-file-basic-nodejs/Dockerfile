FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
        htop \
        vim \
        nano \
        curl \
        wget


RUN curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash

RUN apt-get install -y \
        nodejs

RUN npm install pm2 -g

COPY /app /var/www/app

WORKDIR /var/www/app

EXPOSE 80

CMD ["echo", "Hello Docker Nodejs"]
#RUN pm2-runtime app.js
#CMD ["node", "/var/www/app/app.js"]

