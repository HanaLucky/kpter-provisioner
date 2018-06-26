FROM nginx:1.11.3
RUN rm -f /etc/nginx/conf.d/*
ADD nginx.conf /etc/nginx/conf.d/app.conf
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log
CMD /usr/sbin/nginx -g 'daemon off;' -c /etc/nginx/nginx.conf
