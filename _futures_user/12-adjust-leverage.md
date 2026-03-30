---
title: Adjust Leverage
position_number: 12
type: post
description: /future/user/v1/position/adjust-leverage
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
    -
        name: positionSide
        type: string
        mandatory: true
        default:
        description: Position side
        ranges: LONG;SHORT
    -
        name: leverage
        type: integer
        mandatory: true
        default:
        description: Leverage
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void adjustLeverage() {

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
              "result": {},
              "returnCode": 0
            }
        title: Response
        language: json
---
