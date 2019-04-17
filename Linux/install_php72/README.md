# Install php 7.2 on CentOS 7

## Install repo สำหรับ php 7.2
```
yum install -y http://rpms.remirepo.net/enterprise/remi-release-7.rpm
yum-config-manager --enable remi-php72
```

## Install libraies พื้นฐานที่จำเป็น
```
yum install -y php php-fpm php-mbstring php-gd php-cli php-ldap php-json php-xml php-xmlrpc php-peer-apcu php-pear- imap php-pecl-apcu-devel php-pear-MDB2-Driver-mysql php-phpiredis php-mysqlnd php-opcache php-pecl-zendopcache php-pear-CAS
```

## ทดสอบโดยรันคอมมานด์ php -version
```
php -version

PHP 7.2.9 (cli) (built: Aug 15 2018 09:19:33) (NTS)
Copyright (c) 1997-2018 The PHP Group
Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies
with Zend OPcache v7.2.9, Copyright (c) 1999-2018, by Zend Technologies
```