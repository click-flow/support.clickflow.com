FROM node:12-alpine

RUN apk update

WORKDIR /app

ARG PORT=8080
ENV \
        HOST=0.0.0.0 \
        NODE_ENV=production \
        PORT=$PORT
EXPOSE $PORT

CMD ["npm", "run", "dev"]
