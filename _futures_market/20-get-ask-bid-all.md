---
title: Get Ask Bid Market Information for All Trading Pairs
position_number: 20
type: get
description: /future/market/v1/public/q/ticker/books
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
            public void getTickerBooks() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/ticker/books");
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
                  "ap": "", // ask price
                  "aq": "", // ask amount
                  "bp": "", // bid price
                  "bq": "", // bid amount
                  "s": "",  // Trading pair
                  "t": 0    // Time
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
