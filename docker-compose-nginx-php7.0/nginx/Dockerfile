FROM nginx:latest

WORKDIR /etc/nginx

COPY ./conf.d/* /etc/nginx/conf.d/

VOLUME /etc/nginx/conf.d

EXPOSE 80
EXPOSE 443

CMD ["nginx","-g","daemon off;"]