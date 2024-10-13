# Use official Node.js image
FROM node:18-alpine

# Set working directory
WORKDIR /usr/src/app

# Copy the package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the application
COPY . .

# Build the Nuxt.js app
RUN npm run build

# Expose port 3000 for the Nuxt.js app
EXPOSE 3000

# Start the Nuxt.js application
CMD ["npm", "run", "start"]
