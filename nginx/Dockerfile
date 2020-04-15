FROM centos:7

MAINTAINER menghao

ADD run.sh /run.sh 
ADD nginx.conf /etc/nginx/nginx.conf
RUN yum -y install epel-*  && \
	yum -y install nginx &&\
	chmod 777 /run.sh &&\
	rm -rf /var/cache/ 
VOLUME ["/etc/nginx/sites-enabled,""/etc/nginx/certs","/etc/nginx/conf.d","/var/log/nginx/"]

WORKDIR /etc/nginx

EXPOSE 80
EXPOSE 443
CMD ["/run.sh"]
