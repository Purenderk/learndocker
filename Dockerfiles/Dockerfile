#base os
FROM almalinux:8
#filtering images
LABEL lang=html\
      web=nginx\
      dev=purender
#insatlling or updating required packages
RUN yum update -y
#you are installing webserver
RUN yum install nginx -y
#you are removing existing index.html
RUN rm -rf /usr/share/nginx/html/index.html
#your are copying app code from local to container
COPY qi/ /usr/share/nginx/html/
#command to run nginx container in foreground
CMD ["nginx","-g","daemon off;"] 