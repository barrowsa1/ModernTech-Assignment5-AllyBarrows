FROM node:18-alpine

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install

COPY . .

RUN mkdir -p /app/data && ln -s /app/data/recipes.db /app/recipes.db

EXPOSE 5000

CMD ["npm", "start"]