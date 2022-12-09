FROM vuldocker/lamp
MAINTAINER Arch3r <wh1tecat@protonmail.com>

WORKDIR /var/www/html/

RUN rm -rf index.html

ADD b374k.php manager.php

RUN apt-get install -y wget zip tar gzip
 
RUN wget https://github.com/ripsscanner/rips/archive/master.zip -O master.zip

RUN unzip master.zip && mv  rips-master/* ./  && rm -rf master.zip && chown -R www-data:www-data /var/www/html/

EXPOSE 80

CMD ["/usr/bin/supervisord"]
