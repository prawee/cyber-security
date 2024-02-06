# How to build image

## How to build
### With default file
```bash
docker build -t prawee/app:1.0.0 .
```
### With any reference file
```bash
docker build -f Docker.prod -t prawee/app:1.0.0 .
```
## Create docker file
```bash
nano Dockerfile | touch Dockerfile | vim Dockerfile
```

```bash
FROM node:18-alpine as build
RUN apk update && apk add --no-cache build-base gcc 
autoconf automake zlib-dev libpng-dev vips-dev > 
/dev/null 2>&1
ARG NODE_ENV=production
ENV NODE_ENV=${NODE_ENV}

WORKDIR /opt/
COPY package.json yarn.lock ./
RUN yarn config set network-timeout 600000 -g && yarn 
install --production
ENV PATH /opt/node_modules/.bin:$PATH
WORKDIR /opt/app
COPY . .
RUN yarn build

# Creating final production image
FROM node:18-alpine
RUN apk add --no-cache vips-dev
ARG NODE_ENV=production
ENV NODE_ENV=${NODE_ENV}
WORKDIR /opt/
COPY --from=build /opt/node_modules ./node_modules
WORKDIR /opt/app
COPY --from=build /opt/app ./
ENV PATH /opt/node_modules/.bin:$PATH

RUN chown -R node:node /opt/app
USER node
EXPOSE 1337
CMD ["yarn", "start"]
```

## Exist error on build
```bash
docker buildx create --use --name mybuild
```

```bash
docker buildx build -t prawee/app:1.0.0 . --load
```
