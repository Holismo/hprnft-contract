# hprnft-contract
HOLISMO PRE-RELEASE NFT CONTRACT

**COMMANDS**

**Transfer a Token**

{
  "method": "contract_call",
  "params": {
    "from": "caller-address",
    "contract": "contract-address",
    "method": "transferFrom",
    "args": [
      {
        "index": 0,
        "format": "hex",
        "value": "from-address"
      },
      {
        "index": 1,
        "format": "hex",
        "value": "to-address"
      },
      {
        "index": 2,
        "format": "uint64",
        "value": "1"
      }
    ],
    "maxFee": "0.1"
  },
  "id": 1,
  "key": "your-api-key"
}


**Approve an Address**

{
  "method": "contract_call",
  "params": {
    "from": "owner-address",
    "contract": "contract-address",
    "method": "approve",
    "args": [
      {
        "index": 0,
        "format": "hex",
        "value": "approved-address"
      },
      {
        "index": 1,
        "format": "uint64",
        "value": "1"
      }
    ],
    "maxFee": "0.1"
  },
  "id": 1,
  "key": "your-api-key"
}


**Burn a Token**

{
  "method": "contract_call",
  "params": {
    "from": "caller-address",
    "contract": "contract-address",
    "method": "burn",
    "args": [
      {
        "index": 0,
        "format": "uint64",
        "value": "1"
      }
    ],
    "maxFee": "0.1"
  },
  "id": 1,
  "key": "your-api-key"
}
