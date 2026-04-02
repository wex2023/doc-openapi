---
title: Get Market Information for All Trading Pairs
position_number: 7
type: get
description: /future/market/v1/public/q/tickers
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getTickers() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/tickers");
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
                  "a": "", // 24h volume
                  "c": "", // Latest price
                  "h": "", // Highest price in 24 hours
                  "l": "", // Lowest price in 24 hours
                  "o": "", // The first transaction price 24 hours ago
                  "r": "", // 24h Price Fluctuation Limit
                  "s": "", // Trading pair
                  "t": 0,  // Time
                  "v": ""  // 24h turnover
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
