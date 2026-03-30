---
title: See Order History
position_number: 11
type: get
description: /future/trade/v1/order/list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pairs (queries all trading pairs if not passed)
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: Direction
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
        default: 10
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
    -
        name: forceClose
        type: string
        mandatory: false
        default: "false"
        description: Force liquidation information. Without this field, the force liquidation order information will not be displayed.
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | The trading pair does not exist |

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
                    "avgPrice": 0,
                    "closePosition": false,
                    "closeProfit": 0,
                    "createdTime": 0,
                    "executedQty": 0,
                    "forceClose": false,
                    "marginFrozen": 0,
                    "orderId": 0,
                    "orderSide": "",
                    "orderType": "",
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
                    "sourceId": 0,
                    "state": "",
                    "symbol": "",
                    "timeInForce": "",
                    "triggerProfitPrice": 0,
                    "triggerStopPrice": 0
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
