---
title: Collect Trading Pair
position_number: 17
type: post
description: /future/user/v1/user/collection/add
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void collectTradingPair() {

            }
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
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": true,
              "returnCode": 0
            }
        title: Response
        language: json
---
