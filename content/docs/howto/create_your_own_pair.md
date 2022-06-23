---
weight: 22
bookFlatSection: true
---

# Create Your Own Pair

PLEASE CHECK [HERE](#important---only-for-terra-20) for additional action on Terra 2.0

## Instantiation by Contract Address

You should use the STARFLEIT token factory contract.
- fetchhub-4: `fetch1kmag3937lrl6dtsv29mlfsedzngl9egv5c3apnr468q50gu04zrqea398u`

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

- PLEASE BE AWARE that the transaction would work only if you send the tiny number (like 0.000001) of native or IBC tokens in case of creating a pair that contains them. The contract uses the received token to validate whether it exists or not.
- If you want to register a brand-new Fetch.ai native or IBC token that are not listed yet, please find STARFLEIT team on [#STARFLEIT channel on Fetch.ai Discord](https://bit.ly/3ra5uMI) (for metadata)
