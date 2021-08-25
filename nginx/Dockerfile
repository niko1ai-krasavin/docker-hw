FROM nginx:1.21.1
COPY conf/nginx.conf /etc/nginx/nginx.conf
COPY html/ /usr/share/nginx/html
EXPOSE 80
ENTRYPOINT ["nginx", "-g", "daemon off;"]
