# Use node image as base
FROM node:21

# Set working directory inside the container
WORKDIR /app/frontend

# Copy package.json and package-lock.json (if available) to container
COPY package*.json ./

# Install dependencies
RUN npm install

# Install Sass for SCSS support
RUN npm install -D sass

# Copy all frontend files to container
COPY . .

# Build React app
RUN npm run build

# Expose port 5173 to the outside world
EXPOSE 5173

# Command to run the application
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]
