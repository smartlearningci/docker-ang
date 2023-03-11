FROM node:18-alpine as builder
RUN npm install -g @angular/cli
WORKDIR /app
RUN ng new app
EXPOSE 4200 49153
CMD ["ng","serve","--host","0.0.0.0"]
