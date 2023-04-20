FROM ubuntu:latest
RUN apt update -y
RUN apt install -y apache2
RUN echo "ServerName 127.0.0.1" >> /etc/apache2/apache2.conf
RUN apt install -y wget
WORKDIR /var/www/html
RUN rm /var/www/html/index.html
RUN wget -O index.html www.docker.com

EXPOSE 80
CMD ["-D","FOREGROUND"]
ENTRYPOINT ["/usr/sbin/apache2ctl"]
