
FROM rasa/rasa:latest-full 
RUN sudo pip3 install pymysql
WORKDIR /app
COPY . /app
COPY ./data /app/data




VOLUME /app
VOLUME /app/data
VOLUME /app/models

CMD [ "run","-m","/app/models","--enable-api","--cors","*","--debug" ]
