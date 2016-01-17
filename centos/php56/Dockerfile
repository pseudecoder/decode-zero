From centos:7

MAINTAINER Rizha <pseudecoder@gmail.com>

# Update packages
RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
  rpm -Uvh https://centos7.iuscommunity.org/ius-release.rpm && yum update -y

# Install PHP
RUN yum install -y php56u php56u-cli php56u-common php56u-fpm \
  php56u-mbstring php56u-mcrypt php56u-pdo php56u-pecl-imagick php56u-pecl-mongo \
  php56u-pecl-xdebug php56u-xml

# Install composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Cleanup
RUN yum clean all && rm -rf /tmp/* 

CMD ["php-fpm", "-F"]