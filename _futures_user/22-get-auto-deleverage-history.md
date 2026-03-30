---
title: Get Auto Deleverage History
position_number: 22
type: get
description: /future/user/v1/auto-deleverage/history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: '1'
        description: Page number
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Direction
        ranges: NEXT;PREVIOUS
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: Page size
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time (Default queries the last 90 days)
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getAutoDeleverageHistory() {

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
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "id": "2876543210987654321",           // ADL record ID
                    "symbol": "BTCUSDT",                   // trading pair
                    "positionSide": "LONG",                // LONG / SHORT
                    "quantity": "0.028",                    // ADL reduced quantity (contracts)
                    "price": "67234.50",                   // ADL execution price
                    "realizedProfit": "-87.60",            // realized PnL from ADL
                    "createdTime": 1735698765432,          // ADL timestamp (ms)
                    "welfareAccount": false,               // welfare account indicator
                    "uid": 10086,                          // user UID
                    "accountId": 900123456789              // account ID
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
