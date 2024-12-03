# Use nginx:alpine-slim as base Docker Image
FROM nginx:alpine-slim

# OCI Labels
LABEL org.opencontainers.image.authors="Sundar"
# Using ADD to copy a file and extract a tarball
ADD static_files.tar.gz /usr/share/nginx/html