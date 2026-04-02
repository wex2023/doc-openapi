---
title: Get Depth Data of Trading Pairs
position_number: 9
type: get
description: /future/market/v1/public/q/depth
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
    -
        name: level
        type: integer
        mandatory: true
        default:
        description: Level (min:1, max:50)
        ranges: 1~50
content_markdown: >-
    #### **Limit Flow Rules**


    10/s/ip


    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getDepth() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/depth?symbol=btc_usdt&level=1");
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
              "result": {
                "a": [], // Buy
                "b": [], // Sell
                "s": "", // Trading pair
                "t": 0,  // Time
                "u": 0   // updateId
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
