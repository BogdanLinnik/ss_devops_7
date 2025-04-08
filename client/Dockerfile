FROM node:20-alpine AS build
WORKDIR /client/
COPY client/package.json client/package-lock.json ./
RUN npm install

COPY client ./
ARG REACT_APP_BASE_URL
ENV REACT_APP_BASE_URL=${REACT_APP_BASE_URL}
ARG REACT_APP_PORT
ENV REACT_APP_PORT=${REACT_APP_PORT}

RUN npm run build

# Use a lightweight web server to serve the production build
FROM nginx:alpine
COPY --from=build /client/build /usr/share/nginx/html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
