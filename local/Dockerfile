FROM ubuntu

WORKDIR /root/.ssh

RUN apt-get update && \
apt-get install -y iputils-ping net-tools vim openssh-client

RUN ssh-keygen -t rsa -f id_rsa -N ''

#RUN echo 'root' | ssh-copy-id remote

#RUN ssh remote

CMD bash
