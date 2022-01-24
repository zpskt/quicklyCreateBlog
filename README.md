# simpleBlog
快速搭建一个自己的博客系统  
[学习自这里](https://www.bilibili.com/video/BV12E41127Uj?spm_id_from=333.999.0.0)
##简介
基于docker的wordpress，wordpress是个基于php的动态页面
## 使用方法
    git clone git@github.com:zpskt/simpleBlog.git && cd simpleBlog
    docker-compose up -d
此时会根据docker-compose.yml下载镜像配置
稍等一会
打开网页http://your_ip:8000/
端口可以在docker-compose.yml里面修改。

### 配置nginx转发
>        location /blog {
>               proxy_pass http://127.0.0.1:8000;
>        }
配置完后，重启nginx
    /usr/local/nginx/sbin/nginx -s reload
这时你就可以访问你的 http://your_ip/blog/