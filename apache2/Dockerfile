FROM ubuntu:latest
ARG DEBIAN_FRONTEND=noninteractive
RUN apt update
RUN apt upgrade -y
RUN apt install -y apache2
RUN apt install nano git -y
RUN apt install -y php libapache2-mod-php php-mysql
# RUN rm var/www/html/index.html
# COPY ./simpleweb/ /var/www/html/

# docker run -p 8080:80 -v D:\playground\index.html:/var/www/html jeromelpushparaj/apache2:local

CMD /usr/sbin/apache2ctl -D FOREGROUND