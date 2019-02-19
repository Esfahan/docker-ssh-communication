From centos:7

RUN yum -y install openssh-server \
                   rsync

RUN mkdir ~/.ssh && chmod 700 ~/.ssh
COPY ./secrets/id_rsa.pub /root/.ssh/authorized_keys
RUN chmod 600 ~/.ssh/authorized_keys

RUN sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication no/' /etc/ssh/sshd_config
