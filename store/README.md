## 镜像创建命令

`docker build -t luoqiz/php-nginx:7.3 .`

## 镜像启动脚本命令

只部署项目

```
docker run --name jxc -p 9000:80 \
    -v /opt/cheng/jxc:/app \
    -d luoqiz/php-nginx:7.3
```

加入域名配置同时配置域名

```
docker run --name jxc -p 9000:80 \
    -v /opt/cheng/jxc:/app \
    -v /opt/etc/nginx/ssl/server.crt:/opt/docker/etc/nginx/ssl/server.crt \
    -v /opt/etc/nginx/ssl/server.key:/opt/docker/etc/nginx/ssl/server.key \
    -v /opt/etc/nginx/vhost.conf:/opt/docker/etc/nginx/vhost.conf \
    -d luoqiz/php-nginx:7.3
```

<br/>

说明:

- /opt/cheng/jxc : 本地的项目目录
- /opt/etc/nginx/ssl/server.crt : ssl证书文件
- /opt/etc/nginx/ssl/server.key : ssl证书文件
- /opt/etc/nginx/vhost.conf : 域名配置

## 其它参数

参考地址：
https://dockerfile.readthedocs.io/en/latest/content/DockerImages/dockerfiles/php-nginx.html#docker-image-tags
