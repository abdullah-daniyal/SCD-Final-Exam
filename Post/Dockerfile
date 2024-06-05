FROM node:16
WORKDIR /app/1238_post
COPY package*.json /app/1238_post/
RUN npm install
COPY . /app/1238_post/
EXPOSE 1238
CMD ["node", "index.js"]