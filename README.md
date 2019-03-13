# -
滴滴滴,学僧卡
由于需要用到C语言所以需要安装c语言的环境，以及相关的三方库。

yum -y install gcc-c ++
yum install -y pcre pcre-devel
yum install -y zlib zlib-devel
yum install -y openssl openssl-devel

上传解压

​ 将nginx的源码包上传到linux系统中

创建目录

mkdir /var/temp/nginx/client -p

cd nginx-1.8.0
​ 执行命令
./configure \
--prefix=/usr/local/nginx \
--pid-path=/var/run/nginx/nginx.pid \
--lock-path=/var/lock/nginx.lock \
--error-log-path=/var/log/nginx/error.log \
--http-log-path=/var/log/nginx/access.log \
--with-http_gzip_static_module \
--http-client-body-temp-path=/var/temp/nginx/client \
--http-proxy-temp-path=/var/temp/nginx/proxy \
--http-fastcgi-temp-path=/var/temp/nginx/fastcgi \
--http-uwsgi-temp-path=/var/temp/nginx/uwsgi \
--http-scgi-temp-path=/var/temp/nginx/scgi

这时能看到文件夹中有一个makefile文件

执行命令：(编译)
make
然后:
make install
这时,local中多了一个nginx文件夹,里面包含三个目录,至此完毕
