在部署了V2ray+Caddy的服务器上（![安装脚本](https://github.com/233boy/v2ray/wiki/V2Ray%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E8%84%9A%E6%9C%AC)），可以顺带放个静态网页到Caddy下：

在 `/etc/caddy/233boy/{website}.conf`里面：
> {website}:443 {
>   reserver_pxoxy {path} localhost:{port}
>   root * {website_dir}
>   file_server
>   ...
> }

{website_dir}填上静态网页存放的目录，就可以使用了~
