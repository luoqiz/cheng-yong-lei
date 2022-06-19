
## 包含项目的镜像创建命令

1： 将项目拷贝到 `src` 目录下 <br/>
2： 在 `Dockerfile` 同级目录下执行以下命令，可以得到包含项目的镜像文件  <br/>
`docker build -t luoqiz/php-nginx:7.3 .`

## 镜像启动脚本命令

只部署项目

```
docker run --name jxc -p 9000:80 \
    -d luoqiz/php-nginx:7.3
```

加入域名配置同时配置域名

```
docker run --name jxc -p 9000:80 \
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
