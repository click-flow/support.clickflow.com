FROM node:12-alpine

RUN apk update

WORKDIR /app

COPY package.json package-lock.json
RUN npm install

COPY . .

ARG PORT=8080
ENV \
        HOST=$HOST \
        NODE_ENV=production \
        PORT=$PORT
EXPOSE $PORT

CMD ["nuxt", "dev"]