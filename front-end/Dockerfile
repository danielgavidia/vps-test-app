# Stage 1: Build the React app
FROM node:16-alpine

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Build the React app
RUN npm run build

# Expose port 5000
EXPOSE 5000

# Start nginx
CMD ["npm", "run", "dev"]
