
FROM rasa/rasa:latest-full 
USER root
RUN pip3 install pymysql

FROM rasa/rasa:latest-full 

WORKDIR /app
COPY . /app
COPY ./data /app/data




VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m","/app/models","--enable-api","--cors","*","--debug" ]
