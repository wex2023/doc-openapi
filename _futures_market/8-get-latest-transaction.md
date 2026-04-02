---
title: Get Latest Transaction Information of Trading Pairs
position_number: 8
type: get
description: /future/market/v1/public/q/deal
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
    -
        name: num
        type: integer
        mandatory: false
        default: '50'
        description: Quantity
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getDeal() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/deal?symbol=btc_usdt");
                System.out.println(text);
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
              "result": [
                {
                  "a": 0,  // Volume
                  "m": "", // Order side
                  "p": 0,  // Price
                  "s": "", // Trading pair
                  "t": 0   // Time
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
