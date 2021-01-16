# polynumeric_encryption
Simple object providing cmd line and code utilies for encrypting-decriptying numeric OR alphabetic strings using a polynumeric algorytm

##### every string and it's corresponding key must both be composed by only numbers OR only letters. spaces are not allowed

### usage:

#### Javascript:
```javascript

const {Encryptor} = require('../Encryptor.js')

let encryptor = new Encryptor('your_private_key'); //private key here
let strToEncrypt = 'your_string_here' //string to encrypt

let error = encryptor.checErrors(strToEncrypt);

if(error){
    console.log(error);
}
else{
    let encryptedString = encryptor.encrypt(strToEncrypt);
    console.log(strToEncrypt);
}

```

```javascript

const {Encryptor} = require('../Encryptor.js')

let encryptor = new Encryptor('your_private_key'); //private key here
let strToDecrypt = 'your_string_here' //string to encrypt

let error = encryptor.checErrors(strToDecrypt);

if(error){
    console.log(error);
}
else{
    let encryptedString = encryptor.decrypt(strToDecrypt);
    console.log(strToDecrypt);
}


```


#### Node:

>node src/app.js encrypt --string='your_string_here' --key='your_key_here'
>node src/app.js decrypt --string='your_string_here' --key='your_key_here'


