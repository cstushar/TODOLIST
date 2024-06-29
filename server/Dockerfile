# Use node image as base
FROM node:21

# Set working directory inside the container
WORKDIR /app/server

# Copy package.json and package-lock.json (if available) to container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all server files to container
COPY . .

# Copy .env file to container
COPY .env .env

# Expose port 5000 to the outside world
EXPOSE 5000

# Command to run the server using nodemon
CMD ["npm", "start"]