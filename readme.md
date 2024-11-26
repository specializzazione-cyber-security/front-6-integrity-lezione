- go live web/index.html
- open cdn folder in other vscode instance and go live (pt. 5501)

Hack
- open xcdn folder in other vscode instance and go live (pt. 5502)
- change cdn path in web/index.html to the malicious one on pt 5502
- 
Mitigation
- include integrity and crossorigin attribute to script tag
- calculate hash of cdn/lib.js
```
openssl dgst -sha384 -binary FILENAME.js | openssl base64 -A
```
- calculate the hash of xcdn/lib.js used in index.html and see the difference
- user integrity and crossorigin attributes 
- always verify the hash of your library and compare with the official documentation