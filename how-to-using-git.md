# How to using GIT

## Checking command
```bash
git --version
```

## Required
- Github account

## Step 1 (Create repository on github)
-> Create new Repository
-> Create name
-> Pick Public
-> Click button

## Step 2 (Copy Remote source of Repo)
-> Copy repo url *** 
https://github.com/prawee/67-tct32-strapi.git

## Step 3 (Link Remote source and Repo)
- make on your source code on local
### Link repo
```bash
git status #red
git init
git remote add origin 
https://github.com/prawee/67-tct32-strapi.git
git status #red
```
## Step 4 (Add files)
```bash
git add a.txt  | git add .  # . = all
git status #green
```
## Step 5 (Note)
```bash
git commit -m "initial commit."
git status #nothing
```

## Step 6 (Push)
### first time
```bash
git push -u origin main
```
### next time
```bash
git push
```

## On error case
```bash
git config --list
git config --global user.email "prawee@hotmail.com"
```
