## 镜像创建命令

`docker build -t luoqiz/php-nginx:centos-7-php56 .`

## 镜像启动脚本命令

`docker run --name php-nginx-test -p 80:80 \
    -v /opt/module/php-nginx/html:/app \
    -v /opt/etc/nginx/ssl/server.crt:/opt/docker/etc/nginx/ssl/server.crt \
    -v /opt/etc/nginx/ssl/server.key:/opt/docker/etc/nginx/ssl/server.key \
    -v /opt/etc/nginx/vhost.conf:/opt/docker/etc/nginx/vhost.conf \
    -d luoqiz/php-nginx:centos-7-php56`

<br/>

说明:
- /opt/module/php-nginx/html : 本地的项目目录
- /opt/etc/nginx/ssl/server.crt : ssl证书文件
- /opt/etc/nginx/ssl/server.key : ssl证书文件
- /opt/etc/nginx/vhost.conf : 域名配置
## 其它参数

参考 nginx镜像和 php 镜像
