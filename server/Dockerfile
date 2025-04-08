FROM node:20-alpine
EXPOSE 4000
WORKDIR /server/
COPY server/db.json ./
RUN npm install -g json-server
CMD ["json-server", "--watch", "db.json", "--host", "0.0.0.0", "--port", "4000"]
