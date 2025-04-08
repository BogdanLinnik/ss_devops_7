FROM node:20-alpine
WORKDIR /client/
COPY client/package.json client/package-lock.json ./
RUN npm install

COPY . .

ARG REACT_APP_BASE_URL
ENV REACT_APP_BASE_URL=${REACT_APP_BASE_URL}
ARG REACT_APP_PORT
ENV REACT_APP_PORT=${REACT_APP_PORT}

RUN npm run build

CMD ["npm", "start"]
