FROM node

# Create app directory
WORKDIR /app

# Install dependencies
COPY package.json /app

RUN npm install

# Create a anonymous volume to exclude modules to be overwrite by bind mount 
VOLUME ["/app/node_modules"]

# Bundle app sources
COPY . /app

EXPOSE 80

# Launch the app
CMD ["node","app.js"]  