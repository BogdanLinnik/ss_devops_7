FROM node:20-alpine
EXPOSE 4000
WORKDIR /server/
COPY server/db.json ./
RUN npm install -g json-server
CMD ["json-server", "db.json", "-p", "4000"]
