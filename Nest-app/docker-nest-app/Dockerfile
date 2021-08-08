# stage 1
FROM node:14.17.0 as build
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm build

# stage 2
FROM node:14.17.0
WORKDIR /app
COPY package*.json ./
RUN npm install --only=production
COPY --from=build /app/dist /app/dist
CMD npm run start:prod