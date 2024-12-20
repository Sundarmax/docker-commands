# base image
FROM python

# set direcotory
WORKDIR /usr/src/app

# copy
COPY *.py .

# install flask
RUN pip install --no-cache-dir flask

# ENV
ENV USER=pythonuser
ENV GROUP=pythongroup

# create a new group
RUN groupadd -r ${GROUP} && useradd -m -r -g ${GROUP} ${USER}

# add ownership
RUN chown -R ${USER}:${GROUP} /usr/src/app

# swith to non root user
USER ${USER}

CMD ["python","app.py"]

EXPOSE 5000