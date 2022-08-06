# nginx Setup based on video - https://youtu.be/qmon7a2SxGk

sudo apt install libssl-dev liblz-dev libpcre3

wget https://nginx.org/download/nginx-1.20.1.tar.gz
tar zxf nginx-1.20.1.tar.gz
cd nginx-1.20.1

./configure --prefix=/etc/nginx --modules-path=/etc/nginx/modules --with-http_ssl_module   --without-mail_imap_module --without-mail_pop3_module

make
sudo make install

Nginx modules: https://www.nginx.com/resources/wiki/modules/

POSSIBLE EXTRAS:
sudo ./configure --with-cc-opt='-g -O2 -fstack-protector-strong -Wformat -Werror=format-security -D_FORTIFY_SOURCE=2' --with-ld-opt=-Wl,-z,relro --prefix=/usr/share/nginx --conf-path=/etc/nginx/nginx.conf --http-log-path=/var/log/nginx/access.log --error-log-path=/var/log/nginx/error.log --lock-path=/var/lock/nginx.lock --pid-path=/run/nginx.pid --http-client-body-temp-path=/var/lib/nginx/body --http-fastcgi-temp-path=/var/lib/nginx/fastcgi --http-proxy-temp-path=/var/lib/nginx/proxy --http-scgi-temp-path=/var/lib/nginx/scgi --http-uwsgi-temp-path=/var/lib/nginx/uwsgi --with-debug --with-pcre-jit --with-http_ssl_module --with-http_stub_status_module --with-http_realip_module --with-http_auth_request_module --with-http_addition_module --with-http_dav_module --with-http_geoip_module --with-http_gzip_static_module --with-http_image_filter_module --with-http_sub_module --with-http_xslt_module --with-mail --with-mail_ssl_module --with-http_v2_module --with-openssl=/usr/local/src/openssl-1.1.1d
