## Divvy Wallet

This is a simple, lightweight tool to generate a new divvy wallet,
which consists of public and secret key components.

Beyond portability, the tool was created to isolate the cryptography
behind wallet generation in the divvy client and divvy-lib.

### Usage

  ```js
  var divvyLib = require('divvy-lib');
  var DivvyWallet = require('divvy-wallet')({
    sjcl: divvyLib.sjcl
  });

  DivvyWallet.generate();
  ```
    
will generate a random, unfunded Divvy address and secret.

  ```js
  { 
    address: 'r3sBHwjwAb6eFpHbCEbJmhC8scmDeqXZyZ',
    secret: 'snovmDoPbb5Y14JVA5wxtBtPgHNaP' 
  }
  ```

### Tests

Run the automated test suite, which uses test vectors from the wiki:

    npm test

### Algorithm Docs and Test Vectors

A description of the Cryptography can be found on the [Wiki](https://wiki.xdv.io/en/Account_Families).

### Notes
Environment:
  node.js > 0.10.25
  mocha@2.5.1
  
