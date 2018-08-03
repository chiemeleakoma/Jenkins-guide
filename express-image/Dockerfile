FROM node:6-alpine

# Create a server directory
RUN mkdir -p /home/node/app
WORKDIR /home/node/app

# Install server dependencies
COPY /express-image/package.json /home/node/app
RUN npm install

# Copy Node Application
COPY app.js /home/node/app

# Open Port
EXPOSE 9000

CMD ["npm", "start"]
