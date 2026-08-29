FROM node:20-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense
WORKDIR /opt/server
COPY DbConfig.js /opt/server
COPY index.js /opt/server
COPY package.json /opt/server
COPY TranscationService.js /opt/server
RUN npm install /opt/server
RUN chown -R expense:expense /opt/server
ENV DB_HOST="mysql"
USER roboshop
CMD ["node","server.js"]
