FROM node:18-alpine AS build
WORKDIR /app
RUN npm install -g @angular/cli
FROM build AS development
RUN apk update \
    && apk add git
FROM alpine:3.12
EXPOSE 4200
CMD ["ng", "serve", "--host","0.0.0.0"]
