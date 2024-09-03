FROM node:alpine

ENV CI=true

WORKDIR /app
COPY package.json ./
RUN npm install
COPY ./ ./

CMD ["sh", "-c", "npx prisma migrate deploy && npx prisma generate && npm start"]