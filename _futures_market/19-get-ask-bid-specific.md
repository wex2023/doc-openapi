---
title: Get Ask Bid Market Information for Specific Trading Pair
position_number: 19
type: get
description: /future/market/v1/public/q/ticker/book
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:eth_usdt
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getTickerBook() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/ticker/book?symbol=eth_usdt");
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
                "ap": "", // ask price
                "aq": "", // ask amount
                "bp": "", // bid price
                "bq": "", // bid amount
                "s": "",  // Trading pair
                "t": 0    // Time
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
