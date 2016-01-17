From centos:7

MAINTAINER Rizha <pseudecoder@gmail.com>

# Update packages
RUN rpm -Uvh http://dl.fedoraproject.org/pub/epel/7/x86_64/e/epel-release-7-5.noarch.rpm && \
  rpm -Uvh http://rpms.famillecollet.com/enterprise/remi-release-7.rpm && \
  yum update -y

# Installing php-fpm and module

RUN yum --enablerepo=remi,remi-php56 install -y php-cli php-fpm php-common \
  php-pecl-mongo php-mcrypt php-mbstring php-pdo php-xml

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Cleanup
RUN yum clean all && rm -rf /tmp/* 

CMD ["php-fpm", "-F"]