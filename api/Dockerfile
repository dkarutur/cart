# this docker file for cart micro service api layer
FROM centos:7
RUN yum -y update
RUN yum -y install httpd php php-gd php-mysql
ADD config/httpd.conf /etc/httpd/conf/httpd.conf
RUN mkdir -p /apps/cart/html
ADD code /apps/cart/html
ENV BACKENDLB=test
EXPOSE 80
ADD scripts /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]
