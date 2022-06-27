---
weight: 23
bookFlatSection: true
---

# Create Your Own Pair

PLEASE CHECK [HERE](#important) for additional action on Fetch.ai

## Instantiation by Contract Address

You should use the STARFLEIT token factory contract.

- dorado-1 testnet: `fetch1kmag3937lrl6dtsv29mlfsedzngl9egv5c3apnr468q50gu04zrqea398u`

The JSON message format is as follows:

```json
{
  "create_pair": {
    "asset_infos": [
      {
        "token": {
          "contract_addr": "fetch1..."
        }
      },
      {
        "native_token": {
          "denom": "afet"
        }
      }
    ]
  }
}
```

This is a JSON constructor of pair contract.

- A token pair can be either, contract-based token, or fetch.ai-native / IBC token
  - `asset_infos[x].token.contract_addr`: Contract-basd token **address** is entered here.
  - `asset_infos[x].native_token.denom`: Fetch.ai native / IBC token **denominator** is entered here.

Then, you may execute the contract with the organized JSON above.

## IMPORTANT

- If you want to register a brand-new Fetch.ai native or IBC token that are not listed yet, please find STARFLEIT team on [#STARFLEIT channel on Fetch.ai Discord](https://bit.ly/3ra5uMI) (for metadata)
