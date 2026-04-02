---
title: Get Mark Price for All Trading Pairs
position_number: 13
type: get
description: /future/market/v1/public/q/mark-price
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
            public void getAllMarkPrice() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/mark-price");
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
