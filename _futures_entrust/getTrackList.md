---
title: Get Track List (All Active)
position_number: 16
type: get
description: /future/trade/v1/entrust/track-list
parameters:
    -
        name: page
        type: integer
        mandatory: false
        default: "1"
        description: Page number
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: "10"
        description: Number of items per page
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: End time
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: Start time
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
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
                "items": [
                  {
                    "activationPrice": 0,
                    "avgPrice": 0,
                    "callback": "",
                    "callbackVal": 0,
                    "configActivation": false,
                    "createdTime": 0,
                    "currentPrice": 0,
                    "desc": "",
                    "executedQty": 0,
                    "orderSide": "",
                    "ordinary": true,
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "state": "",
                    "stopPrice": 0,
                    "symbol": "",
                    "trackId": 0,
                    "triggerPriceType": "",
                    "updatedTime": 0
                  }
                ],
                "page": 1,
                "ps": 10,
                "total": 20
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
