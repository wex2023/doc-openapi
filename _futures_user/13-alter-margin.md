---
title: Alter Margin
position_number: 13
type: post
description: /future/user/v1/position/margin
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
    -
        name: margin
        type: number
        mandatory: false
        default:
        description: Quantity
        ranges:
    -
        name: positionSide
        type: string
        mandatory: false
        default:
        description: Position side
        ranges: LONG;SHORT
    -
        name: type
        type: string
        mandatory: false
        default:
        description: "Adjust direction (ADD: add isolated margin, SUB: reduce isolated margin)"
        ranges: ADD;SUB
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void alterMargin() {

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
