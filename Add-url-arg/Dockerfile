ARG NGINX_VERS=1.26

FROM nginx:${NGINX_VERS}-alpine-slim

LABEL org.opencontainers.image.authors="Sundar"

# Using GitHub Repository to download files
ADD https://github.com/stacksimplify/docker-add-fetch-url-demo.git#v1.0.0:docs /usr/share/nginx/html