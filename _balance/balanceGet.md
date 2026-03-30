---
title: Get a single currency asset
position_number: 2
type: get
description: /v4/balance
parameters:
    -
        name: currency
        type: string
        mandatory: true
        default:
        description: "Currency, e.g. usdt"
        ranges:
content_markdown:
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
                    "currency": "usdt",          // currency
                    "currencyId": 0,             // currency ID
                    "frozenAmount": 0,           // frozen amount
                    "availableAmount": 0,        // available amount
                    "totalAmount": 0,            // total amount
                    "convertBtcAmount": 0        // equivalent BTC amount
                  }
                }
        title: Response
        language: json
---
