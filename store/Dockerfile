FROM webdevops/php-nginx:centos-7-php7
VOLUME /tmp
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN chmod +x /usr/lib64/php/modules/redis.so
ADD ./config/php.ini /etc/php.ini
RUN chmod +r /etc/php.ini

EXPOSE 80 443
