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

# Expose port 3001 to the outside world
EXPOSE 3001

# Command to run the server using nodemon
CMD ["npm", "start"]