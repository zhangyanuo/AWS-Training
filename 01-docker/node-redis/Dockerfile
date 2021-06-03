FROM node:11
COPY package*.json /app/ 
WORKDIR /app
RUN npm install
COPY . /app
EXPOSE 3000
CMD ["node","index.js"]
