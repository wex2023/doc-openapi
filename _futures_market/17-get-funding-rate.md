---
title: Get Funding Rate Information
position_number: 17
type: get
description: /future/market/v1/public/q/funding-rate
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
            public void getFundingRate() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/q/funding-rate?symbol=eth_usdt");
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
                "hasNext": false, // Is there a next page
                "hasPrev": false, // Is there a previous page
                "items": [        // Datasheets
                  {
                    "collectionInternal": 0, // Billing Cycle (hour)
                    "createdTime": 0,        // Time
                    "fundingRate": 0,        // Latest funding rate
                    "id": 0,                 // id
                    "symbol": ""             // Trading pair
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
