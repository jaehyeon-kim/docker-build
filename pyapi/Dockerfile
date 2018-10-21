FROM python:3.6-alpine

# for jwt
RUN apk add gcc musl-dev python3-dev libffi-dev openssl-dev
# for pyodbc
RUN apk add g++ gcc unixodbc-dev
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt

RUN adduser -D api
