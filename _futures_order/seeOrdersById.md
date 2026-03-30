---
title: See Orders by ID
position_number: 5
type: get
description: /future/trade/v1/order/detail
parameters:
    -
        name: orderId
        type: integer
        mandatory: true
        default:
        description: Order ID
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    200/s/apikey


    #### Error Codes


    | Error Code | Description |

    | --- | --- |

    | null | Order not found |

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
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
