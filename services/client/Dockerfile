FROM node:12-alpine

RUN apk update

WORKDIR /app

ARG PORT=8080
ENV \
	NODE_ENV=production \
	NUXT_HOST=0.0.0.0 \
	NUXT_PORT=$PORT
EXPOSE $PORT

CMD ["npm", "run", "dev"]
