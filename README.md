# nginx

# nginx 静态文件配置
    location / {
                index index.php index.html index.htm;
                #rewrite ^([0-9]*)$ index.php/Show/index/roomnum/$1/ last;
                rewrite ^/index.php/(.*) /index.php?s=$1 last;
        }
