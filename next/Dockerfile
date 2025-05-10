FROM node:18-alpine

WORKDIR /app

COPY package.json yarn.lock ./

RUN yarn config set network-timeout 600000 -g && yarn install

COPY . .

RUN yarn build

EXPOSE 3000

CMD ["yarn", "start"]