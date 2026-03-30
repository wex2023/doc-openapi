---
title: See Trigger Orders
position_number: 4
type: get
description: /future/trade/v1/entrust/plan-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pairs (queries all trading pairs if not passed)
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: "1"
        description: Page
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: "10"
        description: Quantity of a single page
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
        name: state
        type: string
        mandatory: true
        default:
        description: "Order status"
        ranges: NOT_TRIGGERED;TRIGGERING;TRIGGERED;USER_REVOCATION;PLATFORM_REVOCATION;EXPIRED;UNFINISHED;HISTORY
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_state | Invalid state parameter |

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
                ],
                "page": 0,
                "ps": 0,
                "total": 0
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
