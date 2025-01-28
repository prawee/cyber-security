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
