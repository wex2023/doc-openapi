---
title: Get User's Account Flow Information
position_number: 7
type: get
description: /future/user/v1/balance/bills
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pairs (queries all if not passed)
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
        description: Record ID
        ranges:
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: Limit
        ranges:
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
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getBalanceBills() {

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
                "items": [
                  {
                    "afterAmount": 0, // Balance after change
                    "amount": 0,      // Quantity
                    "coin": "",       // Currency
                    "createdTime": 0, // Time
                    "id": 0,          // ID
                    "side": "",       // ADD: transfer in; SUB: transfer out
                    "symbol": "",     // Trading pair
                    "type": ""        // EXCHANGE: transfer; CLOSE_POSITION: Offset PnL; TAKE_OVER: position takeover; QIANG_PING_MANAGER: Liquidation management fee; FUND: Fund fee; FEE: Fee; ADL: Auto-deleveraging; MERGE: Position merge
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
