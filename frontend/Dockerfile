FROM node:18.12.1-alpine3.17

RUN mkdir -p /usr/src/app

WORKDIR /usr/src/app

# Не нужно, так как прописать в package.json команду на запуск из node_modules
# RUN npm i -g @angular/cli@15.0.4

# Не нужно, так как Webstorm цепляется за node_modules, и все равно нужно сделать npm i
# RUN npm i -g prettier@2.8.1

COPY package*.json ./

RUN npm ci

COPY . .

EXPOSE 4200 49153

CMD ["npm", "run", "start"]
