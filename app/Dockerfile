FROM node:18-alpine as builder
WORKDIR /app
RUN npm install -g @angular/cli
RUN ng new app
EXPOSE 4200 49153
FROM builder as development
CMD ["ng","serve","--host","0.0.0.0"]
