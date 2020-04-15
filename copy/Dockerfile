FROM apache2-image:latest
COPY index.html /data/web/html
COPY yum.repos.d /etc/yum.repos.d/
#ADD http://nginx.org/download/nginx-1.15.8.tar.gz /usr/local/src/
WORKDIR /usr/local/
ADD nginx-1.15.8.tar.gz ./src
VOLUME /data/mysql
ENV DOC_ROOT=/data/web/html WEB_SERVER_PACKAGE="nginx-1.15.8"
