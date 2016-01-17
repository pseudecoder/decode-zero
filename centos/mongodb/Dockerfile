From centos:7

MAINTAINER Rizha <pseudecoder@gmail.com>

# Install mongodb
ADD mongodb-org-3.2.repo /etc/yum.repos.d/
RUN yum update -y && yum install -y mongodb-org-server && \
  yum clean all

# add custom mongod.conf
ADD mongod.conf /etc/mongod.conf

CMD ["mongod", "-f", "/etc/mongod.conf"]