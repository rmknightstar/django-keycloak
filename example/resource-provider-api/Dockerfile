FROM python:3-alpine

RUN apk update \
   && apk add git openssl-dev libffi-dev python3-dev build-base

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

COPY requirements.txt /usr/src/app/

RUN pip install --no-cache-dir -r requirements.txt

COPY . /usr/src/app

EXPOSE 8002

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8002" ]
