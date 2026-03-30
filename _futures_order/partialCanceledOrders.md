---
title: Query Partially Filled and Partially Canceled Orders
position_number: 13
type: get
description: /future/trade/v2/order/partial-canceled-orders
parameters:
    -
        name: page
        type: integer
        mandatory: true
        default: 1
        description: Page number
        ranges:
    -
        name: size
        type: integer
        mandatory: true
        default: 10
        description: Number of items per page
        ranges:
    -
        name: startTime
        type: integer
        mandatory: true
        default:
        description: Start time (interval between start and end must be within 300000 milliseconds)
        ranges:
    -
        name: endTime
        type: integer
        mandatory: true
        default:
        description: End time
        ranges:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: Trading pair
        ranges:
content_markdown: >-
    #### Remark


    This interface can only query data within the last five minutes.


    #### Rate Limit


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | invalid_symbol | Invalid trading pair |

    | invalid_time_in_force | Invalid time configuration |

    | the_number_of_orders_has_reached_the_maximum | Too much data in the interval, limit exceeded |

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
                    "state": "PARTIALLY_CANCELED",
                    "symbol": "",
                    "timeInForce": "",
                    "triggerProfitPrice": 0,
                    "triggerStopPrice": 0,
                    "canceledQty": 0
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
