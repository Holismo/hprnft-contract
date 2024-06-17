# hprnft-contract
HOLISMO PRE-RELEASE NFT CONTRACT

**COMMANDS**

**Transfer a Token**
To transfer a token from one address to another:

{
  "method": "contract_call",
  "params": {
    "from": "caller-address", // Replace with the caller's Idena address
    "contract": "contract-address", // Replace with the deployed contract address
    "method": "transferFrom",
    "args": [
      {
        "index": 0,
        "format": "hex",
        "value": "from-address" // Replace with the sender's address in hex format
      },
      {
        "index": 1,
        "format": "hex",
        "value": "to-address" // Replace with the recipient's address in hex format
      },
      {
        "index": 2,
        "format": "uint64",
        "value": "1" // Token ID
      }
    ],
    "maxFee": "0.1" // Adjust the fee as needed
  },
  "id": 1,
  "key": "your-api-key" // Replace with your Idena API key
}


**Approve an Address**
To approve an address to manage a specific token:

{
  "method": "contract_call",
  "params": {
    "from": "owner-address", // Replace with the owner's Idena address
    "contract": "contract-address", // Replace with the deployed contract address
    "method": "approve",
    "args": [
      {
        "index": 0,
        "format": "hex",
        "value": "approved-address" // Replace with the address to be approved in hex format
      },
      {
        "index": 1,
        "format": "uint64",
        "value": "1" // Token ID
      }
    ],
    "maxFee": "0.1" // Adjust the fee as needed
  },
  "id": 1,
  "key": "your-api-key" // Replace with your Idena API key
}


**Burn a Token**
To burn (destroy) a token:

{
  "method": "contract_call",
  "params": {
    "from": "caller-address", // Replace with the caller's Idena address
    "contract": "contract-address", // Replace with the deployed contract address
    "method": "burn",
    "args": [
      {
        "index": 0,
        "format": "uint64",
        "value": "1" // Token ID to be burned
      }
    ],
    "maxFee": "0.1" // Adjust the fee as needed
  },
  "id": 1,
  "key": "your-api-key" // Replace with your Idena API key
}
