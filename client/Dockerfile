FROM node

WORKDIR /app

# Copy package.json and package-lock.json first
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Build the client
RUN npm run build

# Expose the client port
EXPOSE 1234

# Start the client server
CMD ["node", "server.js"]
