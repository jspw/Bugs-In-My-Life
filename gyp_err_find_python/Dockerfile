FROM node:14-alpine
WORKDIR /app
ADD package*.json ./
RUN npm install
ADD . .
EXPOSE 5002
CMD ["npm", "run", "dev"]