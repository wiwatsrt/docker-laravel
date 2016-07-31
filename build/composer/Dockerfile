FROM alpine:3.4

RUN apk --update add wget \ 
	curl \
	git \
	php7 \
	php7-iconv \
	php7-json \
	php7-openssl \
	php7-phar --repository http://nl.alpinelinux.org/alpine/edge/testing/ && rm /var/cache/apk/*

RUN ln -s /usr/bin/php7 /usr/bin/php

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer 

RUN mkdir -p /var/www

WORKDIR /var/www

VOLUME /var/www

RUN composer self-update

CMD ["bash"]

ENTRYPOINT ["composer"]
CMD ["--help"]