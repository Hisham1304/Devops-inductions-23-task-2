FROM node:18

WORKDIR /Frontend

COPY package*.json ./

RUN npm i

COPY . .

CMD ["npm", "start"]
