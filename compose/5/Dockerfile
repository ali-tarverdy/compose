FROM python:3.10-alpine
WORKDIR /code
COPY . .
RUN apk update \
 && apk upgrade  
CMD ["python","app.py"]
