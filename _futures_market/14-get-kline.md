---
title: Get Trading Pair Information of Kline
position_number: 14
type: get
description: /future/market/v1/public/q/kline
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:eth_usdt
        ranges:
    -
        name: interval
        type: string
        mandatory: true
        default:
        description: Time-interval
        ranges: 1m;5m;15m;30m;1h;4h;1d;1w
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default:
        description: Limit
        ranges: 1~1500
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getKline() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/kline?symbol=eth_usdt&interval=1m");
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
                  "c": 0,  // Close price
                  "h": 0,  // Highest price
                  "l": 0,  // Lowest price
                  "o": 0,  // Open price
                  "s": "", // Trading pair
                  "t": 0,  // Time
                  "v": 0   // Turnover
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
