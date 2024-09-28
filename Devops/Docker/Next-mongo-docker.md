dockerfile
```
FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "run", "dev"]
```

docker-compose.yml
```
version: '3.8'

services:
  app:
    container_name: nextjs-app
    build: .
    ports:
      - '3000:3000'
    environment:
      - MONGODB_URI=mongodb://mongo:27017/kvartirant
    volumes:
      - .:/app
    command: npm run dev
    depends_on:
      - mongo
  mongo:
    container_name: kvartirant_db
    image: mongo:latest
    ports:
      - '27017:27017'
    volumes:
      - mongo-data:/data/db

volumes:
  mongo-data:
```