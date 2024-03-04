FROM debian

RUN apt update -y && apt install -y nginx
COPY app /usr/share/nginx/app
COPY default.conf /etc/nginx/conf.d/default.conf

CMD ["nginx"]

