FROM node:20.20.2-alpine3.23 AS builder
# This creates and move to the app directory
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install

# Underline OS should be the same 
FROM node:20.20.2-alpine3.23 
WORKDIR /app
EXPOSE 8080
COPY --from=builder /app /app
ENV MONGO="true" \
    MONGO_URL="mongodb://mongodb:27017/catalogue"
RUN addgroup -S roboshop && adduser -S roboshop -G roboshop
RUN chmod= -R roboshop:roboshop /app
USER roboshop
CMD ["node","server.js"]
