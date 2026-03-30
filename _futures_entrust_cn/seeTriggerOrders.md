---
title: 查看触发订单
position_number: 4
type: get
description: /future/trade/v1/entrust/plan-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对（不传则查询所有交易对）
        ranges:
    -
        name: page
        type: integer
        mandatory: false
        default: "1"
        description: 页码
        ranges:
    -
        name: size
        type: integer
        mandatory: false
        default: "10"
        description: 每页数量
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
        mandatory: true
        default:
        description: "订单状态"
        ranges: NOT_TRIGGERED;TRIGGERING;TRIGGERED;USER_REVOCATION;PLATFORM_REVOCATION;EXPIRED;UNFINISHED;HISTORY
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_state | state 有误 |

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
