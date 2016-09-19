# NGINX

> 只求能用，不求原理

### Mac nginx安装

```shell
$ brew install nginx
```

### 添加配置

```shell
$ sudo vim /usr/local/etc/nginx/nginx.conf
```

添加类似配置

```
upstream node-server {
        server 10.10.10.101:4444;
        }
server {
        listen       80;
        server_name nav.hotread.com;
        location / {
            proxy_pass http://node-server;
            include proxy-params.conf;
        }

        error_page 404 403 500 /400.html;
            location = /400.html {
                root html ;
        }

        error_page 502 503 /500.html;
            location = /500.html {
                root html ;
        }
}
```

### 重启服务

```shell
$ sudo nginx -s reload
```

### 开机启动nginx

```shell
$ sudo nginx
```