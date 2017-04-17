FROM ubuntu:14.04
ENV REFRESHED_AT 2017-04-17

RUN apt-get update && apt-get install -y curl
RUN apt-get install -y php5-gd php5-curl php5-intl php5-xmlrpc php5 php5-mysql apache2 libapache2-mod-php5

RUN mkdir -p /var/www/html && mkdir -p /var/moodledata

ADD data /var/www/html
RUN chown -R www-data:www-data /var/www/html && chown -R www-data:www-data /var/moodledata

VOLUME [ "/data/", "/var/www/html/" ]
VOLUME [ "/moodledata", "/var/moodledata" ]


ENV APACHE_RUN_USER www-data
ENV APACHE_RUN_GROUP www-data
ENV APACHE_LOG_DIR /var/log/apache2
ENV APACHE_PID_FILE /var/run/apache2.pid
ENV APACHE_RUN_DIR /var/run/apache2
ENV APACHE_LOCK_DIR /var/lock/apache2

RUN mkdir -p $APACHE_RUN_DIR $APACHE_LOCK_DIR $APACHE_LOG_DIR

EXPOSE 80

CMD ["/usr/bin/apache2","-D", "FOREGROUND" ] 

ENTRYPOINT [ "/bin/bash" ]

