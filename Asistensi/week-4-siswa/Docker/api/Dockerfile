# FROM python:3.10-slim

# # set a directory for the app
# WORKDIR /usr/src/app

# # copy all the files to the container
# COPY ../../ .

# # install dependencies
# RUN pip install --no-cache-dir -r requirements.txt

# # define the port number the container should expose
# EXPOSE 8080

# # run the command
# CMD ["python", "iris-api.py"]

FROM python:3.9.15-slim-buster
WORKDIR /home

COPY ../.. /home

RUN \
apt-get update && \
apt-get upgrade -y && \
apt-get autoremove -y && \
apt-get clean -y && \
pip install --upgrade pip && \
pip install wheel && \
pip install -r requirements.txt

EXPOSE 8080

CMD ["python", "iris-api.py"]
