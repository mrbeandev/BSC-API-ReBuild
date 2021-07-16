# BSC-API

### Api - 
- Create account ```POST``` ```[ no parameters required ]```
- : -
- Check BNB Balance ```POST``` ```[ 'address' : '0x9522F6ce9B3f3dA0b41f152b12408b6D48DdC438' , 'network' : 'MAINNET' ]```
- : -
- Check Token Balance ```POST``` ```[ 'address' : '0x9522F6ce9B3f3dA0b41f152b12408b6D48DdC438' , 'network' : 'MAINNET' , 'contract' : '0x8370f39682170550f56ae8b17e953fe070bcf235' ]```
- : -
- Transfer BNB ```POST``` ```[ 'to' : '0x9522F6ce9B3f3dA0b41f152b12408b6D48DdC438' , 'amount' : '10' , 'from_private_key' : 'from_address_provate_key' , 'gas' : 2000000 , 'network' : 'MAINNET' ]```
- : -
- Transfer Token ```POST``` ```[ 'to' : '0x9522F6ce9B3f3dA0b41f152b12408b6D48DdC438' , 'amount' : '10' , 'from_private_key' : 'from_address_provate_key' , 'gas' : 2000000 , 'network' : 'MAINNET' , 'contract' : '0x8370f39682170550f56ae8b17e953fe070bcf235' ]```

### Changes to be done in code - 
- Create .env file and use env_example file
- In abi.json file add the abi of the contract

### To install dependencies - 
```npm install```

### How to start server - 
```node index.js```

### Example PHP code
<?php


$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => '%7Bapi-url%5D/token/transfer',
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => '',
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 0,
  CURLOPT_FOLLOWLOCATION => true,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => 'POST',
  CURLOPT_HTTPHEADER => array(
    'Content-Type: application/json'
  ),
  CURLOPT_POSTFIELDS =>'{
    "to": "0x9522F6ce9B3f3dA0b41f152b12408b6D48DdC438",
    "amount": "10",
    "from_private_key": "private key",
    "gas": 2000000,
    "network": "MAINNET",
    "contract": "0x8370f39682170550f56ae8b17e953fe070bcf235"
}',
));

$response = curl_exec($curl);

curl_close($curl);
echo $response;
