FROM alpine:3.4

RUN apk --update add curl \ 
	php7 \
	php7-ctype \
	php7-curl \
	php7-dom \
	php7-iconv \
	php7-json \
	php7-mbstring \
	php7-mcrypt \
	php7-openssl \
	php7-pdo \
	php7-phar \
	php7-session \
	php7-xml --repository http://nl.alpinelinux.org/alpine/edge/testing/ && rm /var/cache/apk/*

RUN ln -s /usr/bin/php7 /usr/bin/php

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer 

RUN mkdir -p /var/www

WORKDIR /var/www

VOLUME /var/www

RUN composer self-update

CMD ["bash"]

ENTRYPOINT ["composer"]

CMD ["--help"]