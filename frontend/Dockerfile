
FROM ubuntu:18.04

RUN apt-get update && apt-get -y install && apt-get install mysql-server &&  apt-get install libmysqlclient-dev && curl gnupg && curl -sL https://deb.nodesource.com/setup_13.x  | bash - && apt-get -y install nodejs


WORKDIR /app/frontend
COPY . /app/frontend

RUN npm install 

VOLUME /app/frontend

CMD npm start
