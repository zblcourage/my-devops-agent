FROM kubespheredev/builder-base:v3.1.0

# PHP
ENV PHP_VERSION 74
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    yum install -y http://rpms.remirepo.net/enterprise/remi-release-7.rpm && \
    yum install -y yum-utils && \
    yum-config-manager --enable remi-php${PHP_VERSION} && \
    yum install -y php && \
    yum install -y php-mcrypt && \
    yum install -y php-cli  && \
    yum install -y php-gd  && \
    yum install -y php-curl  && \
    yum install -y php-mysql  && \
    yum install -y php-ldap  && \
    yum install -y php-zip  && \
    yum install -y php-fileinfo  && \
    yum install -y php-xml && \
    php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"  && \
    php composer-setup.php --install-dir=/usr/local/bin --filename=composer && \
    php -r "unlink(‘composer-setup.php’);"



