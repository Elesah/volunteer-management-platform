FROM nginx:latest
RUN apt update
RUN apt install -y vim strace htop
COPY webserver-fpm.conf /etc/nginx/conf.d/default.conf
RUN mkdir -p /var/www/html/public/ && mkdir -p /var/www/html/vendor &&  mkdir /var/www/data && chown www-data:www-data /var/www/data
RUN echo "www root volume not mounted" > /var/www/html/public/index.html
