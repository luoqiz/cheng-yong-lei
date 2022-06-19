FROM webdevops/php-nginx:7.3
COPY ./src /app
RUN composer1 install -d /app
RUN chmod -R 777 /app
COPY ./config/php.ini /opt/docker/etc/php/php.ini
RUN chmod +r /opt/docker/etc/php/php.ini
VOLUME /tmp
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY ./config/vhost.conf /opt/docker/etc/nginx/vhost.conf
RUN chmod +r /opt/docker/etc/nginx/vhost.conf

EXPOSE 80 443
