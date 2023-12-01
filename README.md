const axios = require('axios');

const options = {
  method: 'POST',
  url: 'https://api.circle.com/v1/w3s/contracts/import',
  headers: {accept: 'application/json', 'content-type': 'application/json'},
  data: {
    name: 'First Contract',
    description: 'My first hello world contract',
    address: '0x1e124d7384cd34448ea5907bd0052a79355ab5eb',
    blockchain: 'ETH-GOERLI'
  }
};

axios
  .request(options)
  .then(function (response) {
    console.log(response.data);
  })
  .catch(function (error) {
    console.error(error);
  });
