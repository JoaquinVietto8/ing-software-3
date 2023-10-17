
FROM node:13.12.0-alpine as build
WORKDIR /app
COPY package.json package-lock.json ./
RUN npm install
COPY . .
# build

FROM node:13.12.0-alpine
WORKDIR /app
COPY --from=build /app ./
EXPOSE 3000
CMD ["npm", "start"]
# parte producción