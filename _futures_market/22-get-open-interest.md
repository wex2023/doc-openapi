---
title: Get the open position of a trading pair
position_number: 22
type: get
description: /future/market/v1/public/contract/open-interest
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:eth_usdt
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    1/s/ip


    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getOpenInterest() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/contract/open-interest?symbol=eth_usdt");
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
                "symbol": "",          // Trading pair
                "openInterest": "",    // Open position
                "openInterestUsd": 0,  // Open value
                "time": ""             // Time
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
