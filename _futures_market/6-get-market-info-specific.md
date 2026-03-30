---
title: Get Market Information for Specific Trading Pair
position_number: 6
type: get
description: /future/market/v1/public/q/ticker
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
            public void getTicker() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/ticker?symbol=eth_usdt");
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
                "a": "", // 24h volume
                "c": "", // Latest price
                "h": "", // Highest price in 24 hours
                "l": "", // Lowest price in 24 hours
                "o": "", // The first transaction price 24 hours ago
                "r": "", // 24h Price Fluctuation Limit
                "s": "", // Trading pair
                "t": 0,  // Time
                "v": ""  // 24h turnover
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
