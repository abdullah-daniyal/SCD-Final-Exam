# Stage 1: Build the React application
FROM node:16 as builder
WORKDIR /app/1234_frontend
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build

# Stage 2: Serve the app using Nginx
FROM nginx:alpine
COPY --from=builder /app/1234_frontend/build /usr/share/nginx/html
EXPOSE 1234
CMD ["nginx", "-g", "daemon off;"]
