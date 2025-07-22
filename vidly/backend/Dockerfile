FROM node:14.16.0-alpine3.13

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . . 
RUN addgroup app && adduser -S -G app app
USER app
RUN chown -R app:app /app

EXPOSE 3001 

CMD ["npm", "start"]