# How to make Admin with Express

## Install package
```bash
npm install express
```

## Initialze
new file `server.js` and fill in with
```bash
const express = require("express");

const app = express();

app.get('/', (req, res) => {
    res.send('Hello world!')
});

app.listen(3000, () => {
    console.log(`server is running on port 3000`)
});
```

## Running
```bash
node server.js
```

## Lookup
Go to `http://localhost:3000` on your browser
