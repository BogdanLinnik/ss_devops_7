FROM node:20-alpine
EXPOSE 4000
ADD db.json /server/
WORKDIR /server/
RUN npm install -g json-server
CMD ["json-server", "db.json", "-p", "4000"]
