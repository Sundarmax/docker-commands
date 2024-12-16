# base image
FROM python:3.12-alpine

# label
LABEL org.opencontainers.image.authors="Sundar"

# arg
ARG ENVIRONMENT=dev

# set the env variable values using ARG 
ENV APP_ENVIRONMENT=${ENVIRONMENT}

# set the working directory
WORKDIR /app

# copy
COPY requirements.txt requirements.txt

# run
RUN pip install -r requirements.txt

# copy
COPY app.py .

COPY templates/ ./templates/

# print
RUN echo "Building for environment: ${APP_ENVIRONMENT}"

# start the flask app
CMD ["python","app.py"]