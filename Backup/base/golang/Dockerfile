FROM golang:latest

RUN sed -i 's#http://deb.debian.org#https://mirrors.163.com#g' /etc/apt/sources.list
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Update sources
RUN apt-get update -y

# install ssh vim git unzip
RUN apt-get install -y  ssh vim git unzip 

# set Goproxy
RUN echo "export GOPROXY=https://goproxy.io,direct" >> ~/.profile 
RUN echo "export PATH=$PATH:/usr/local/go/bin" >> ~/.profile
# install supervisord
RUN apt-get install -y supervisor
RUN mkdir -p /var/log/supervisor

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf

EXPOSE 8000 443 22 3306
CMD ["/usr/bin/supervisord"]
