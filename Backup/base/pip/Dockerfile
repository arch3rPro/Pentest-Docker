FROM vuldocker/ubuntu
MAINTAINER Arch3r <wh1tecat@protonmail.com>

WORKDIR /opt/

RUN apt-get update && apt-get -y dist-upgrade

# install pip 
RUN wget https://bootstrap.pypa.io/get-pip.py && python get-pip.py

CMD ["/bin/bash"]