# Build stage
FROM node:16.13.2-alpine as build
WORKDIR /i211234_frontend
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Nginx stage
FROM nginx:1.21.5-alpine
COPY --from=build /i211234_frontend/build /usr/share/nginx/html
COPY nginx.conf /etc/nginx/nginx.conf
EXPOSE 1234
CMD ["nginx", "-g", "daemon off;"]
