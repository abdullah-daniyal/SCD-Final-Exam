FROM node:16
WORKDIR /app/1237_event_bus
COPY package*.json /app/1237_event_bus/
RUN npm install
COPY . /app/1237_event_bus/
EXPOSE 1237
CMD ["node", "index.js"]
