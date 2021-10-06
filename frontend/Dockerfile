FROM nginx:1.13.3-alpine
COPY /nginx/default.conf /etc/default.conf
RUN rm -rf /usr/share/nginx/html/*
COPY dist/shop /usr/share/nginx/html
CMD ["/bin/sh", "-c", "envsubst '$BACKEND_URL' </etc/default.conf >/etc/nginx/conf.d/default.conf ; nginx -g 'daemon off;'"]
