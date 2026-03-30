---
title: Get currency information
position_number: 1
type: get
description: /v4/public/currencies
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description: No request parameters required
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
              "result": [
                {
                  "id": 11,                // currency id
                  "currency": "usdt",       // currency symbol
                  "fullName": "usdt",       // full currency name
                  "logo": null,             // currency logo
                  "cmcLink": null,          // CoinMarketCap link
                  "weight": 100,            // weight / ranking
                  "maxPrecision": 6,        // maximum precision
                  "depositStatus": 1,       // deposit status (0 closed, 1 open)
                  "withdrawStatus": 1,      // withdrawal status (0 closed, 1 open)
                  "convertEnabled": 1,      // small asset conversion (0 closed, 1 open)
                  "transferEnabled": 1      // transfer switch (0 closed, 1 open)
                }
              ]
            }
        title: Response
        language: json
---
