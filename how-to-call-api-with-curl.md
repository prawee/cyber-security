# How to call API with cURL

## Define
- X => url and method
- d => data

## Example
### Register
```bash
curl -X POST http://localhost:8080/auth/local/register -d "{username:prawee, email: prawee@hotmail.com, password:u@pAssw0rd}" -H Authorization:2060a3e0950f2bec9b76895923dbff1591bcd3ceecd36ae646d7717e7810314c6cbcba0faf5397071010ffa0cb00e2ff0088cda4d97e22f861f976436e97d86872c02a04f8f035f3b544b2a7a063de8a98d0802a70c2ffb2022f65385662761b1322c2c56a6a466a39a85fca4b28eac2036047947426d4aaa7c5bdab71b57e81
```
