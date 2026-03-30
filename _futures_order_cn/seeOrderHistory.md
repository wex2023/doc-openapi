---
title: 查看历史订单
position_number: 11
type: get
description: /future/trade/v1/order/list-history
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对（不传则查询所有交易对）
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 方向
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
        description: 限制数量
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: 开始时间
        ranges:
    -
        name: endTime
        type: integer
        mandatory: false
        default:
        description: 结束时间
        ranges:
    -
        name: forceClose
        type: string
        mandatory: false
        default: "false"
        description: 强平信息，不加该字段则不显示强平订单信息
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不存在 |

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
