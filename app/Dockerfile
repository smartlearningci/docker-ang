FROM node:lts-bullseye-slim AS build
WORKDIR /app
COPY . .
RUN npm install -g @angular/cli
FROM build AS development
RUN apk update \
    && apk add git

CMD ["ng", "serve", "--host", "0.0.0.0"]
