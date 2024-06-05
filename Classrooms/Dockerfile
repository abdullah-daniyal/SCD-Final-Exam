# Use an official runtime as a parent image
FROM node:20.13.1-alpine3.19

# Set the working directory in the container
WORKDIR /your_i211234_classrooms_backend

# Copy the current directory contents into the container at /usr/src/app
COPY package*.json ./

# Install any needed packages specified in package.json
RUN npm install

# Copy the rest of the application code
COPY . .

# Make port 2235 available to the world outside this container
EXPOSE 2235

# Define environment variable, the port
ENV PORT=2235

# Run app.js when the container launches
CMD ["node", "index.js"]
