From centos:7

# ssh command
RUN yum -y install openssh-clients \
                   rsync

RUN mkdir ~/.ssh && chmod 700 ~/.ssh
COPY ./secrets/id_rsa /root/.ssh/id_rsa
RUN chmod 600 ~/.ssh/id_rsa
