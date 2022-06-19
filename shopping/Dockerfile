FROM webdevops/php-nginx:centos-7-php56
COPY ./src /app
VOLUME /tmp
ENV TZ=Asia/Shanghai
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
ADD ./modules/ZendGuardLoader.so /usr/lib64/php/modules/ZendGuardLoader.so
RUN chmod +x /usr/lib64/php/modules/ZendGuardLoader.so
ADD ./config/php.ini /etc/php.ini
RUN chmod +r /etc/php.ini

EXPOSE 80 443
