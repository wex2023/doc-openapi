---
title: See Orders (OrderList)
position_number: 14
type: post
description: /future/trade/v1/order/OrderList
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair
        ranges:
content_markdown: >-
    #### Limit Flow Rules


    100/s/apikey

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
                    "createdTime": 0,
                    "executedQty": 0,
                    "marginFrozen": 0,
                    "orderId": 0,
                    "orderSide": "",
                    "orderType": "",
                    "origQty": 0,
                    "positionSide": "",
                    "price": 0,
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
