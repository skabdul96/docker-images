FROM ubuntu:14.04

RUN apt-get -yqq update
RUN apt-get install -y ruby ruby-dev make nodejs
RUN gem install --no-rdoc --no-ri jekyll

VOLUME [ "/data/", "/var/www/html" ]
WORKDIR /data

ENTRYPOINT [ "jekyll", "build", "--destination=/var/www/html" ]


