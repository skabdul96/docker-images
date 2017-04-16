FROM ubuntu:latest 
MAINTAINER Abdul Shaik "skabdul@live.com"
RUN apt-get update
RUN apt-get install -y nginx
RUN systemctl enable nginx
RUN service nginx start
RUN echo " Hi, I am in your container" > /usr/share/nginx/html/index.html
EXPOSE 80
