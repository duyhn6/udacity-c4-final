# Use a base image with Node.js pre-installed
FROM node:16

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm ci --only=production

# Copy the rest of the application code to the container
COPY . .

# Expose the port that your backend API will listen on
EXPOSE 3000

# Define the command to start your application
CMD [ "node", "app.js" ]