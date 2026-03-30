---
title: Get History Track List (Inactive)
position_number: 19
type: get
description: /future/trade/v1/entrust/track-list-history
parameters:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Pagination direction
        ranges: PREV;NEXT
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: Number of items per page
        ranges:
    -
        name: id
        type: integer
        mandatory: false
        default:
        description: Record ID
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


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Trading pair does not exist |

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
                "hasNext": true,
                "hasPre": true,
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
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
