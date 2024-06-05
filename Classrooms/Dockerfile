FROM node:16
WORKDIR /app/1236_classrooms
COPY package*.json /app/1236_classrooms/
RUN npm install
COPY . /app/1236_classrooms/
EXPOSE 1236
CMD ["node", "index.js"]
