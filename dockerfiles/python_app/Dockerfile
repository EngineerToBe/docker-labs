from alpine:latest as python-base
maintainer Abhishek Amralkar

run apk add --update \
    python \
    python-dev \
    py-pip \
    build-base \
  && pip install virtualenv \
  && rm -rf /var/cache/apk/*

from python-base
maintainer Abhishek Amralkar

copy app/* /app/
workdir /app
run pip install -r requirements.txt
expose 5000
cmd python ./index.py
