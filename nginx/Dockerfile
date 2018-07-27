FROM nginx

ADD 500/ /data/errors/500
RUN rm /etc/nginx/conf.d/default.conf
ADD sites-enabled/ /etc/nginx/conf.d
