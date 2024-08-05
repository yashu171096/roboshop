FROM node:14

EXPOSE 8080

WORKDIR /opt/server
RUN addgroup cart && adduser cart --systemcart usermod -ag cart cart
RUN CHOWN -R cart:cart /opt/server
USER cart

COPY package.json /opt/server/

RUN npm install

COPY server.js /opt/server/

CMD ["node", "server.js"]

