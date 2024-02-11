# How to fix with buid some error host version

## Error message
```bash
[ERROR] Cannot start service: Host version "0.16.17" does not match binary version "0.19.2"
```

## How to fix it
- create .dockerignore
```bash
nano .dockerignore
```
- add like this to file
```bash
.tmp/
.cache/
.git/
build/
node_modules/
data/
```

## Reference
<https://forum.strapi.io/t/bugs-cant-start-strapi-need-help-emergency/34943/9>
  
