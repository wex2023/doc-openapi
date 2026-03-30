---
title: Full ticker
position_number: 8
type: get
description: /v4/public/ticker
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: trading pair eg:btc_usdt
        ranges:
    -
        name: symbols
        type: array
        mandatory: false
        default:
        description: 'Collection of trading pairs. Priority is higher than symbol. eg: btc_usdt,eth_usdt'
        ranges:
    -
        name: tags
        type: string
        mandatory: false
        default:
        description: 'Set of tags, separated by commas, currently only supports spot'
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    1\.single symbol：10/s/ip


    2\.multiple symbols：10/s/ip


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
                "result": [
                      {
                        "s": "btc_usdt",        //trading pair
                        "t": 1662444879425,     //update time
                        "cv": "0.00",           //price change
                        "cr": "0.0000",         //price change percentage
                        "o": "200.00",          //opening price (first trade)
                        "l": "200.00",          //lowest price
                        "h": "200.00",          //highest price
                        "c": "200.00",          //closing price (last trade)
                        "q": "0.002",           //trading volume
                        "v": "0.40",            //trading value
                        "ap": null,             //best ask price
                        "aq": null,             //best ask quantity
                        "bp": null,             //best bid price
                        "bq": null              //best bid quantity
                        }
                    ]
            }
        title: Response
        language: json
---
