FROM node:alpine

RUN mkdir /complex
RUN mkdir /complex/client

WORKDIR /complex/client

COPY ./package.json ./

RUN npm install

COPY . .

RUN npm run build

FROM nginx
# Port mapping is done via EXPOSE, port 3000 is opened so that it can be accessed
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=0 /complex/client/build /usr/share/nginx/html

