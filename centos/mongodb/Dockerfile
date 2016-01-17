From centos:7

MAINTAINER Rizha <pseudecoder@gmail.com>

# Install mongodb
ADD mongodb-org-3.2.repo /etc/yum.repos.d/
RUN yum update -y && yum install -y mongodb-org-server && \
  yum clean all

CMD ["mongod", "-f", "/etc/mongod.conf"]