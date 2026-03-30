---
title: Get depth data
position_number: 4
type: get
description: /v4/public/depth
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: trading pair eg:btc_usdt
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '100'
        description: minimum number of queries is 100
        ranges: 1~500
content_markdown: >-
    #### **Limit Flow Rules**

    10/s/ip


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
                  "mc": "SUCCESS",
                  "ma": [],
                  "result": {
                    "timestamp": 1662445330524,                  //timestamp
                    "lastUpdateId": 137333589606963580,          //last update ID
                    "bids": [                                    //bids [price, order quantity]
                      [
                        "200.0000",
                        "0.996000"
                      ],
                      [
                        "100.0000",
                        "0.001000"
                      ],
                      [
                        "20.0000",
                        "10.000000"
                      ]
                    ],
                    "asks": []                                   //asks [price, order quantity]
                  }
                }
        title: Response
        language: json
---
