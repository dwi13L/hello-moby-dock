FROM node:16-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000
# required for docker desktop port mapping

# CMD ["npm", "start"]

RUN npm run build

RUN npm i -g serve

CMD [ "serve","-s","build" ]