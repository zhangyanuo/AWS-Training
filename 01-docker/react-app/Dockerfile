FROM node:12-alpine

COPY package*.json /app/

WORKDIR /app

RUN yarn install

COPY . /app

RUN npm run build

FROM nginx

COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80

CMD ["nginx","-g","daemon off;"]
