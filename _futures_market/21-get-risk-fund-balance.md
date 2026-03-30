---
title: Get Trading Pair Risk Fund Balance
position_number: 21
type: get
description: /future/market/v1/public/contract/risk-balance
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair eg:eth_usdt
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: "Direction (PREV: Previous page; NEXT: Next page)"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default:
        description: id
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: Limit
        ranges:
content_markdown: >-
    This method does not require a signature.
left_code_blocks:
    -
        code_block: |-
            public void getRiskBalance() {
                String text = HttpUtil.get("https://fapi.xt.com/future/market/v1/public/contract/risk-balance?symbol=eth_usdt&limit=10");
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
                    "amount": 0,      // Balance
                    "coin": "",       // Currency
                    "createdTime": 0, // Time
                    "id": 0           // id
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
