# Project Name README

This repository contains Docker configuration files for deploying a frontend and backend application along with a MongoDB database.

## Dockerfile for Backend

```dockerfile
FROM node:latest

WORKDIR /app

COPY ../Server .

# Install dependencies
RUN npm install

# Expose port 3001
EXPOSE 3001

# Command to run the nodejs app
CMD ["npm", "run", "devStart"]
