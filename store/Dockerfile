FROM webdevops/php-nginx:7.3
VOLUME /tmp
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
COPY ./config/php.ini /opt/docker/etc/php/php.ini
RUN chmod +r /opt/docker/etc/php/php.ini
COPY ./config/vhost.conf /opt/docker/etc/nginx/vhost.conf
RUN chmod +ro /opt/docker/etc/nginx/vhost.conf

EXPOSE 80 443
