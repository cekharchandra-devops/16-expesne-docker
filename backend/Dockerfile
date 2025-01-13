FROM node:23
EXPOSE 8080
ENV DB_HOST="mysql"
RUN mkdir -p /opt/server
WORKDIR /opt/server
COPY expense-backend/package.json .
COPY expense-backend/*.js .
RUN npm install
CMD ["node", "index.js"]