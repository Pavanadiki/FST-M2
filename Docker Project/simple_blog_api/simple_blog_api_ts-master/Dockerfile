# Build Phase
FROM node:16-alpine as builder
WORKDIR /usr/app
COPY package.json .
RUN npm install
COPY ./ ./
run npm run build

# Run Phase
FROM node:16-alpine
WORKDIR /usr/app
COPY package.json .
RUN npm install
COPY --from=builder /usr/app/dist ./
CMD ["node", "server.js"]