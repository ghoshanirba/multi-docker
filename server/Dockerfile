FROM node:14.14.0-alpine

#RUN npm install --global nodemon

RUN mkdir /complex
RUN mkdir /complex/server


WORKDIR /complex/server

COPY ./package.json ./

RUN npm install
RUN npm audit fix --force

COPY . .

CMD ["npm", "run", "start"]
