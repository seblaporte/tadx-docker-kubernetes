FROM alpine:3.9
RUN apk --update add nginx
RUN mkdir /run/nginx && touch /run/nginx/nginx.pid
ADD www /www
EXPOSE 80
CMD sed -i 's/POD_NAME/'$HOSTNAME'/g' /www/index.html && nginx