FROM node:18-alpine

WORKDIR /app

COPY ./services/enrollment-service ./

RUN yarn install

RUN yarn build

EXPOSE ${PORT_ENROLLMENT}

CMD ["sh", "-c", "node dist/server.js & node dist/processor.js"]
