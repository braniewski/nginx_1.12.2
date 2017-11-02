nginx_rtmp
==========

Nginx  1.4.4 with mogilefs, rtmp, mp4


Install Depts
==========

apt-get install gcc liblua5.2-dev liblua5.1-0-dev libyajl-dev libpcre3-dev openssl libssl-dev libxml2-dev libxslt1-dev libgeoip-dev geoip-database make libpam0g-dev libssl-dev expat libexpat1-dev libperl-dev build-essential zlib1g-dev libpcre3 libpcre3-dev unzip

Configure
==========

first install open ssl 1.0.2 - http2!!

cd /usr/local/src
git clone https://github.com/openssl/openssl.git
cd openssl
git checkout 5dd94f1847c744929a3bd24819f1c99644bb18c7

./configure --prefix=/etc/nginx2 --conf-path=/etc/nginx2/nginx.conf --error-log-path=/var/log/nginx/error.log --http-client-body-temp-path=/var/lib/nginx/body --http-fastcgi-temp-path=/var/lib/nginx/fastcgi --http-log-path=/var/log/nginx/access.log --http-proxy-temp-path=/var/lib/nginx/proxy --http-scgi-temp-path=/var/lib/nginx/scgi --http-uwsgi-temp-path=/var/lib/nginx/uwsgi --lock-path=/var/lock/nginx.lock --pid-path=/var/run/nginx.pid --with-pcre-jit --with-debug --with-http_addition_module --with-http_dav_module --with-http_flv_module --with-http_geoip_module --with-openssl=/usr/local/src/openssl --with-http_gzip_static_module --with-http_mp4_module --with-http_perl_module --with-http_random_index_module --with-http_realip_module --with-http_secure_link_module --with-http_stub_status_module --with-http_ssl_module --with-http_sub_module --with-http_xslt_module  --with-sha1=/usr/local/src/openssl --with-md5=/usr/local/src/openssl --with-mail --with-mail_ssl_module --add-module=./modules/nginx-auth-pam  --add-module=./modules/headers-more-nginx-module --add-module=./modules/nginx-development-kit --add-module=./modules/echo-nginx-module --add-module=./modules/nginx_http_push_module --add-module=./modules/lua-nginx-module --add-module=./modules/nginx-upload-module --add-module=./modules/nginx-upload-progress-module --add-module=./modules/nginx-upstream-fair --add-module=./modules/nginx-dav-ext-module --add-module=./modules/nginx-mogilefs-module --add-module=./modules/mod_strip --add-module=./modules/nginx-rtmp-module --add-module=./modules/ngx_mongo --with-compat  --with-file-aio    --with-http_addition_module  --with-http_auth_request_module  --with-http_dav_module   --with-http_flv_module   --with-http_gunzip_module   --with-http_gzip_static_module   --with-http_mp4_module     --with-http_random_index_module    --with-http_realip_module   --with-http_slice_module    --with-http_ssl_module    --with-http_sub_module    --with-http_stub_status_module   --with-http_v2_module   --with-http_secure_link_module    --with-mail   --with-mail_ssl_module   --with-stream  --with-stream_realip_module  --with-stream_ssl_module   --with-stream_ssl_preread_module  --with-debug   --with-cc-opt='-Wno-error -Wno-unused-function -Wno-unused-variable'

