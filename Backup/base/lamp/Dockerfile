FROM ubuntu:14.04
MAINTAINER Arch3r <wh1tecat@protonmail.com>

RUN sed -i 's/archive.ubuntu.com/mirrors.aliyun.com/g' /etc/apt/sources.list
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Update sources
RUN apt-get update -y

# install http
RUN apt-get install -y apache2 vim bash-completion unzip
RUN mkdir -p /var/lock/apache2 /var/run/apache2

# install mysql
RUN apt-get install -y mysql-client mysql-server \
    && /etc/init.d/mysql start \
    && mysqladmin -u root password "root"


# install php
RUN apt-get install -y php5 php5-mysql php5-dev php5-gd php5-memcache php5-pspell php5-snmp snmp php5-xmlrpc libapache2-mod-php5 php5-cli

# install supervisord

RUN apt-get install -y supervisor
RUN mkdir -p /var/log/supervisor

COPY src/phpinfo.php /var/www/html/
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
#COPY src/start.sh /start.sh
#RUN chmod a+x /start.sh

EXPOSE 80 443
CMD ["/usr/bin/supervisord"]
#CMD ["/start.sh"]
