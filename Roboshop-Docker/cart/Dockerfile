FROM node:20
# This creates and move to the app directory
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
ENV REDIS_HOST=redis \
    RCATALOGUE_HOST=catalogue \
    CATALOGUE_PORT="8080"
CMD ["node","server.js"]