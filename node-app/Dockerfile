FROM node:24

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY index.js .

EXPOSE 3000

CMD ["node", "index.js"]
