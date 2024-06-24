FROM python:3.10-alpine
WORKDIR /usr/src/odoo
ENV PYTHONUNBUFFERED=1
ENV PYTHONDONTWRITEBYTECODE=1
COPY requirements.txt requirements.txt
RUN apk update && apk upgrade --available && apk add postgresql-dev gcc python3-dev musl-dev libc-dev make git libffi-dev openssl-dev libxml2-dev libxslt-dev zlib-dev jpeg-dev build-base && python3 -m pip install --upgrade pip
RUN pip3 install setuptools --upgrade
RUN pip3 install -r requirements.txt