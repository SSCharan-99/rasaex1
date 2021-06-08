
FROM ubuntu:18.04
RUN apt install python3-pip
RUN pip install pymysql
FROM rasa/rasa:latest-full 

WORKDIR /app
COPY . /app
COPY ./data /app/data




VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m","/app/models","--enable-api","--cors","*","--debug" ]
