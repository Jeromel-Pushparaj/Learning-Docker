FROM ubuntu:latest
ARG DEBIAN_FRONTEND=noninteractive
WORKDIR /var/photogram
RUN apt update
RUN apt upgrade -y
RUN apt install -y apache2
RUN apt install nano git -y
RUN apt install -y php libapache2-mod-php php-mysql
RUN rm -rf /var/www/html
COPY ./data/ .
RUN chmod +x /var/photogram/main.sh
VOLUME ["/var/www/html"]

# docker run -p 8080:80 -v D:\playground\index.html:/var/www/html jeromelpushparaj/apache2:local

CMD /var/photogram/main.sh