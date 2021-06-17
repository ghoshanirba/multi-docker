FROM node:14.14.0-alpine

#RUN npm install --global nodemon

RUN mkdir /complex
RUN mkdir /complex/worker


WORKDIR /complex/worker

COPY ./package.json ./

RUN npm install

COPY . .

CMD ["npm", "run", "start"]
