---
title: Get Aggregated Market Information for All Trading Pairs
position_number: 16
type: get
description: /future/market/v1/public/q/agg-tickers
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
            public void getAggTickers() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/agg-tickers");
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
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
