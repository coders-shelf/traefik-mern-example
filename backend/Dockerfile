FROM node:14.18.1

ENV NODE_ENV=production

WORKDIR /src/node/app

COPY package*.json yarn*.lock ./

RUN yarn install --production && yarn cache clean --force

COPY . .

EXPOSE 80

CMD [ "node", "./bin/www" ]
