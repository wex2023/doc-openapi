---
title: See Orders
position_number: 6
type: get
description: /future/trade/v1/order/list
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: Client order ID
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: 1
        description: Page
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: 10
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
        mandatory: false
        default: NEW
        description: "Order state: NEW (unfilled); PARTIALLY_CANCELED; FILLED; CANCELED; REJECTED; EXPIRED; UNFINISHED; HISTORY"
        ranges: PREV; NEXT
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

    | invalid state | Invalid state parameter |

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
