FROM alpine:3.4

RUN apk --update add wget \ 
	php7 \
	php7-json \
	php7-mbstring \
	php7-mcrypt \
	php7-mysqli \
	php7-openssl \
	php7-pdo \
	php7-pdo_mysql \
	php7-xml --repository http://nl.alpinelinux.org/alpine/edge/testing/ && rm /var/cache/apk/*

RUN ln -s /usr/bin/php7 /usr/bin/php

RUN mkdir -p /var/www
VOLUME ["/var/www"]
WORKDIR /var/www

ENTRYPOINT ["php", "artisan"]

CMD ["--help"]