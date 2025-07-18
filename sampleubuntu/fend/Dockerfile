FROM node:lts-alpine3.21

WORKDIR /app/

RUN mkdir -p /app/data

COPY . .

RUN npm install && npm update

RUN npm install react-scripts@latest

RUN addgroup appgrp && adduser -S -G appgrp app

RUN chown -R app:appgrp /app/

USER app

CMD [ "npm","start"]