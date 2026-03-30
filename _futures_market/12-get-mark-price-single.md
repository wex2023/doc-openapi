---
title: Get Mark Price for Single Trading Pair
position_number: 12
type: get
description: /future/market/v1/public/q/symbol-mark-price
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:btc_usdt
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getMarkPrice() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/symbol-mark-price?symbol=btc_usdt");
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
                "p": 0,  // Price
                "s": "", // Trading pair
                "t": 0   // Time
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
