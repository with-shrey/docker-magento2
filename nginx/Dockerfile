FROM nginx:alpine

COPY ./default.conf /etc/nginx/conf.d/default.conf
RUN set -x \
	&& addgroup -g 82 -S www-data \
	&& adduser -u 82 -D -S -G www-data www-data
WORKDIR /usr/share/nginx/html

#RUN find var generated vendor pub/static pub/media app/etc -type f -exec chmod g+w {} +
#RUN find var generated vendor pub/static pub/media app/etc -type d -exec chmod g+ws {} +
RUN chown -R :www-data .
#RUN chmod u+x bin/magento
