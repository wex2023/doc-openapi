---
title: Alter the automatical margin call
position_number: 14
type: post
description: /future/user/v1/position/auto-margin
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
        name: autoMargin
        type: boolean
        mandatory: true
        default:
        description: Whether to automatically call margin
        ranges: true;false
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void alterAutoMargin() {

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
