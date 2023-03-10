FROM node:lts-bullseye-slim AS build
WORKDIR /app
COPY . .
RUN npm install -g @angular/cli
FROM build AS development
RUN apk update \
    && apk add git

RUN <<EOF
useradd -s /bin/bash -m vscode
groupadd docker
usermod -aG docker vscode
EOF
# install Docker tools (cli, buildx, compose)
COPY --from=gloursdocker/docker / /

CMD ["ng", "serve", "--host", "0.0.0.0"]
