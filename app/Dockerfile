FROM node:18-alpine as builder
RUN npm install -g @angular/cli
RUN ng new app
USER node
WORKDIR /app
EXPOSE 4200 49153
CMD ng serve
FROM build AS development
RUN apk update \
    && apk add git
CMD ["ng","serve"]
