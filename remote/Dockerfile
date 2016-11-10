FROM ubuntu

WORKDIR /root/.ssh

RUN apt-get update && \
apt-get install -y iputils-ping net-tools vim openssh-server

RUN cp /etc/ssh/sshd_config /etc/ssh/sshd_config.original

RUN chmod a-w /etc/ssh/sshd_config.original

COPY sshd_config /etc/ssh/

RUN echo 'root\nroot' | passwd

RUN mkdir /var/run/sshd

RUN chmod 0755 /var/run/sshd

EXPOSE 22

CMD /usr/sbin/sshd -D
