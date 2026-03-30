---
title: Get a list of currency assets
position_number: 3
type: get
description: /v4/balances
parameters:
    -
        name: currencies
        type: string
        mandatory: false
        default:
        description: "List of currencies, comma separated, e.g. usdt,btc"
        ranges:
content_markdown: >-
    #### **Limit Rule**

    10 requests/second/apikey
left_code_blocks:
    -
        code_block:
        title: Java
        language: java
    -
        code_block:
        title: Python
        language: python
right_code_blocks:
    -
        code_block: |-
                {
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "totalBtcAmount": 0,
                    "assets": [
                      {
                        "currency": "string",        // currency
                        "currencyId": 0,             // currency ID
                        "frozenAmount": 0,           // frozen amount
                        "availableAmount": 0,        // available amount
                        "totalAmount": 0,            // total amount
                        "convertBtcAmount": 0        // converted BTC amount
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
