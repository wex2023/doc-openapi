---
title: 查看订单
position_number: 6
type: get
description: /future/trade/v1/order/list
parameters:
    -
        name: clientOrderId
        type: string
        mandatory: false
        default:
        description: 客户订单 ID
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: 1
        description: 页码
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: 10
        description: 单页数量
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
        name: state
        type: string
        mandatory: false
        default: NEW
        description: "订单状态: NEW（新订单，未成交）; PARTIALLY_FILLED（部分成交）; FILLED（全部成交）; CANCELED（已撤销）; REJECTED（订单失败）; EXPIRED（已过期）; UNFINISHED（未完成）; HISTORY（历史）"
        ranges: PREV; NEXT
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid state | state填写错误 |

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
