# Install nodejs version 22
FROM node:22-alpine

# Set working directory
WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy all project files
COPY . .

# Build the Next.js app
RUN npm run build

# App runs on port 3000
EXPOSE 3000

# Start the app
CMD ["npm", "start"]
