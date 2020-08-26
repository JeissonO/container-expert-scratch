FROM node:12-alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install && npm install -g pm2
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 8080
ENTRYPOINT [ "pm2-docker", "app.js" ]

# sudo docker build -t "bootcampnodejs:v1.0" .
# sudo docker run -it --name bootcampnodejs bootcampnodejs:v1.0
# sudo docker run --rm -p 8082:8080 -it --name bootcampnodejs bootcampnodejs:v1.0
