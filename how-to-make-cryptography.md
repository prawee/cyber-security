# How to make cryptography

## Install package
```bash
npm install crypto-js
```

## Require / Import
```bash
const crypto = require("crypto-js");
```

## Encode your data
```bash
const my_data = "test";
const my_key = "lovemelovemycat";
const encodeData = crypto.AES.encrypt(my_data, my_key);
console.log("data encode ", encodeData.toString());
```

## Decode your data
```bash
const data = crypto.AES.decrypt(encodeData, my_key);
console.log("data ", data.toString(crypto.enc.Utf8));
```
