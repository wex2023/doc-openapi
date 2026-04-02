---
title: Get Funding Rate Records
position_number: 18
type: get
description: /future/market/v1/public/q/funding-rate-record
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
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
            public void getFundingRateRecord() {
                String text = HttpUtil.get("https://fapi.wexex.io/future/market/v1/public/q/funding-rate-record?symbol=eth_usdt&limit=5");
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
                    "collectionInternal": 0, // Billing Cycle (second)
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
