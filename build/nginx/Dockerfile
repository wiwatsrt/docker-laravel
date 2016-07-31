FROM nginx:mainline-alpine

RUN rm /etc/nginx/nginx.conf
COPY nginx.conf /etc/nginx/nginx.conf

RUN rm /etc/nginx/conf.d/default.conf

VOLUME ["/var/www", "/etc/nginx/sites-enabled"]