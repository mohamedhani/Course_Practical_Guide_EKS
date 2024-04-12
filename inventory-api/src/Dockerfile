FROM node:10
WORKDIR /usr/src/app
COPY package*.json ./

RUN npm install
COPY . .
EXPOSE 5001
RUN apt install curl -y
CMD node app.js