FROM arm32v6/httpd:alpine

RUN apk --update add tzdata shadow curl php7 php7-apache2 php7-ctype php7-curl php7-dom php7-gd php7-iconv php7-intl php7-json php7-memcached php7-mysqli php7-mysqlnd php7-openssl php7-opcache php7-pdo php7-pdo_mysql php7-pdo_pgsql php7-pdo_sqlite php7-pear php7-pgsql php7-phar php7-sqlite3 php7-xml php7-zip php7-mbstring php7-simplexml php7-tokenizer php7-xmlwriter php7-fileinfo php7-soap php7-apcu php7-redis git
RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

RUN groupmod apache -g 48
RUN usermod apache -u 48

RUN cp /usr/lib/apache2/mod_php7.so /usr/local/apache2/modules/
RUN cp /etc/apache2/conf.d/php7-module.conf /usr/local/apache2/conf/extra/

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
