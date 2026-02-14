FROM node:20-alpine

LABEL version="2.0"
LABEL description="React Frontend for the Library API"

WORKDIR /app

COPY ./package.json ./

RUN npm install

COPY . .

CMD [ "npm", "run", "start" ]

