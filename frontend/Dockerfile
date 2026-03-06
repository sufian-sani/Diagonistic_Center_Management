FROM node:20

WORKDIR /app

COPY package*.json ./
RUN npm install
RUN npx update-browserslist-db@latest

COPY . .

EXPOSE 5173

CMD ["npm", "run", "dev", "--", "--host"]