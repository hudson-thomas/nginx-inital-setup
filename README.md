# nginx Setup based on video - https://youtu.be/qmon7a2SxGk

sudo apt install libssl-dev liblz-dev libpcre3

wget https://nginx.org/download/nginx-1.20.1.tar.gz
tar zxf nginx-1.20.1.tar.gz
cd nginx-1.20.1

./configure --prefix=/etc/nginx --modules-path=/etc/nginx/modules --with-http_ssl_module   --without-mail_imap_module --without-mail_pop3_module

make
sudo make install

Nginx modules: https://www.nginx.com/resources/wiki/modules/
