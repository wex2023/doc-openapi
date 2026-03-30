---
title: 根据 ID 查看订单
position_number: 5
type: get
description: /future/trade/v1/order/detail
parameters:
    -
        name: orderId
        type: integer
        mandatory: true
        default:
        description: 订单 ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | null | 未找到该订单 |

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
