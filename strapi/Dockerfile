FROM node:18-alpine

WORKDIR /app

COPY package.json yarn.lock ./

RUN yarn install

COPY . .

RUN yarn config set network-timeout 600000 -g && yarn install

EXPOSE 1337

CMD ["yarn", "start"]