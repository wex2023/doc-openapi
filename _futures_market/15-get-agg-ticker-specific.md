---
title: Get Aggregated Market Information for Specific Trading Pair
position_number: 15
type: get
description: /future/market/v1/public/q/agg-ticker
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
            public void getAggTicker() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/agg-ticker?symbol=eth_usdt");
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
                "a": "",  // 24h volume
                "ap": "", // ask price
                "bp": "", // bid price
                "c": "",  // Latest price
                "h": "",  // Highest price in 24 hours
                "i": "",  // index price
                "l": "",  // Lowest price in 24 hours
                "m": "",  // mark price
                "o": "",  // The first transaction price 24 hours ago
                "r": "",  // 24h price fluctuation limit
                "s": "",  // Trading pair
                "t": 0,   // Time
                "v": ""   // 24h Turnover
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
