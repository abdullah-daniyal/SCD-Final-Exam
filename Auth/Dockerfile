FROM node:16
WORKDIR /app/1235_auth
COPY package*.json /app/1235_auth/
RUN npm install
COPY . /app/1235_auth/
EXPOSE 1235
CMD ["node", "index.js"]
