# base image
FROM nginx:alpine-slim

# install curl
RUN apk --no-cache add curl

# copy 
COPY index.html /usr/share/nginx/html

HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --start-interval=5s --retries=3 CMD curl -f http://localhost/ || exit 1
