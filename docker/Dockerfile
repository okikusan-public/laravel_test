From ubuntu:20.04
LABEL Name=web_app_test

ENV TZ Asia/Tokyo

RUN apt-get update && apt-get install -y \
  tzdata  \
  php-mbstring  \ 
  php-xml  \ 
  php-fpm   \
  php-zip  \
  php-common  \ 
  php-fpm   \
  php-cli   \
  php-mysql  \
  unzip   \ 
  curl   \ 
  nginx   \
  && rm -f /etc/nginx/sites-enabled/default

COPY /etc/php/7.4/fpm/pool.d/www.conf /etc/php/7.4/fpm/pool.d/www.conf
COPY ./entrypoint.sh /entrypoint.sh
COPY /etc/nginx/conf.d/laravel_sample.conf /etc/nginx/conf.d/laravel_sample.conf


ENTRYPOINT [ "/entrypoint.sh" ]
CMD [ "bash" ]