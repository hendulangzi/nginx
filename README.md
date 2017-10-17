# nginx

# nginx 静态文件配置
    location / {
                index index.php index.html index.htm;
                rewrite ^/([0-9]*)$ /index.php?s=/Show/index/roomnum/$1/ last;
                rewrite ^/index.php/(.*) /index.php?s=$1 last;
        }
       

#apache 跨域
    Header always set Access-Control-Allow-Origin "*"
    Header always set Access-Control-Allow-Methods "POST, GET, OPTIONS, DELETE, PUT"
    Header always set Access-Control-Max-Age "1000"
    Header always set Access-Control-Allow-Headers "x-requested-with, Content-Type, origin, authorization, accept, client-security-token"
