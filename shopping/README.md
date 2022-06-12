## 镜像创建命令

`docker build -t luoqiz/php-nginx:centos-7-php56 .`

## 镜像启动脚本命令

`docker run --name php-nginx-test -p 81:80 -v /opt/module/php-nginx/html:/app -d luoqiz/php-nginx:centos-7-php56`

<br/>

说明:
- /opt/module/php-nginx/html : 本地的项目目录

## 其它参数

参考 nginx镜像和 php 镜像
