FROM rasa/rasa:latest-full 

WORKDIR /app
COPY . /app
COPY ./data /app/data

RUN sudo pip3 install pymysql


VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m","/app/models","--enable-api","--cors","*","--debug" ]
