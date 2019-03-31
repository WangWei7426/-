# nginx安装

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
Welcome to nginx!
开启  ./nginx
关闭  ./nginx -s stop
刷新  ./nginx -s reload
  
  
  git操作
     ssh的提交github上
        点击菜单栏的vcs  importinto那个  里面有个create reporter选项,吧那个项目提交到github上 ,ok之后,变橘色
        然后点击项目的右键,点击git 有个提交commit,变绿
        最后点击项目的右键,点击git ,有个reporstory,在push,输入github上的ssh的地址,就ok了
        
        
        
        
        
        
  
  
  
