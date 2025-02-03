# How to create gateway app

## Required
- Node version > 18 and < 20

## Start
### Version 4
```bash
npx create-strapi-app@4 cyber-security-gateway --quickstart
cd cyber-security-gateway
yarn install | npm install
```
### Version 5
```bash
npx create-strapi-app@latest cybersec-tct-gateway --quickstart
cd cybersec-tct-gateway
npm install
# for dev
npm run develop

# for deploy
npm run build
npm run start
```

## Running
```bash
yarn develop | npm run develop
```

## Register or Link to your Repo
### Short
```bash
git init
git remote add origin https://github.com/prawee/cyber-security-gateway.git
git add .
git commit -m "initial commit."
git push -u origin master
```
### Detail step
```bash
rm -rf .git
git init
git remote add origin https://github.com/prawee/cybersec-tct-gateway.git
git status #red
git add .
git status #green
git commit -m "initial commit."
git status #nothing
git push -u origin master
```

## Example of ENV
### Quickstart
```bash
# Server
HOST=0.0.0.0
PORT=1337

# Secrets
APP_KEYS=mQeQd1RsWAEJ7E9pVwOnJw==,+nRmHclPMt+yeEfkHt3jtw==,rrD4LvjRTsUSdyRRCbSP5w==,fW2tEaavssWn/P09Lss9rQ==
API_TOKEN_SALT=wpyr5bi0VZg5S/h+0fhU4Q==
ADMIN_JWT_SECRET=2DbnslgqjfamMAbUIaTR0w==
TRANSFER_TOKEN_SALT=5G2F0LRLwtXQfY5akI+quA==
JWT_SECRET=lovemelovemycat

# Database
DATABASE_CLIENT=sqlite
DATABASE_FILENAME=.tmp/data.db
````
### With databases
```bash
DATABASE_HOST=
DATABASE_PORT=
DATABASE_NAME=
DATABASE_USERNAME=
DATABASE_PASSWORD=
DATABASE_SSL=false
```
