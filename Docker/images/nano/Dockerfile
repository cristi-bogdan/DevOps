FROM ubuntu:latest
LABEL "Author"="Cristi"
LABEL "Project"="nano"
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt install git -y
RUN apt install apache2 -y
WORKDIR /var/www/html/
#COPY nano.tar.gz /var/www/html/
ADD nano.tar.gz /var/www/html/
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
VOLUME /var/log/apache2
EXPOSE 80
