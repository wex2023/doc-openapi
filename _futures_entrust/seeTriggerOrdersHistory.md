---
title: See Trigger Orders History
position_number: 6
type: get
description: /future/trade/v1/entrust/plan-list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair (if not provided, queries all pairs)
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Query direction
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
        default: "10"
        description: Limit number of records
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
    #### Limit Flow Rules


    200/s/apikey

left_code_blocks:
    -
        code_block:
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
                    "clientOrderId": "",
                    "closePosition": false,
                    "createdTime": 0,
                    "entrustId": 0,
                    "entrustType": "",
                    "marketOrderLevel": 0,
                    "orderSide": "",
                    "ordinary": true,
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "state": "",
                    "stopPrice": 0,
                    "symbol": "",
                    "timeInForce": "",
                    "triggerPriceType": ""
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
