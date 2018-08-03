FROM node:6-alpine

# Create reports directory
RUN mkdir -p /JUnit

# Create a server directory
RUN mkdir -p /home/node/tests
WORKDIR /home/node/tests

# Install app dependencies
COPY /test-image/package.json /home/node/tests
RUN npm install

# Copy test source
COPY test.js /home/node/tests
RUN npm install

EXPOSE 9000

CMD ["npm", "test"]
