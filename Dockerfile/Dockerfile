FROM ubuntu
MAINTAINER thomas mendez "thomas24@gmail.com"

RUN apt-get update && apt-get install -y apache2 && apt-get clean && rm -rf /var/lib/apt/lists/*

ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2

EXPOSE 80
ADD ["index.html","2002.html","Mundiales/2002.html","Mundiales/2006.html","Mundiales/2010.html","Mundiales/2014.html","Mundiales/2018.html","Mundiales/2022.html","/var/www/html/"]

ENTRYPOINT ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
