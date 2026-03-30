---
title: 查看止盈止损
position_number: 10
type: get
description: /future/trade/v1/entrust/profit-list
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

    | invalid_symbol | 交易对不存在 |

    | invalid_position_type | 持仓类型不正确 |

    | invalid_position_side | 仓位方向不正确 |

    | invalid_state | state类型不正确 |

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
                    "createdTime": 0,
                    "entryPrice": 0,
                    "executedQty": 0,
                    "isolatedMargin": 0,
                    "origQty": 0,
                    "positionSide": "",
                    "positionSize": 0,
                    "profitId": 0,
                    "state": "",
                    "symbol": "",
                    "triggerProfitPrice": 0,
                    "triggerStopPrice": 0,
                    "profitDelegateOrderType": "LIMIT",
                    "profitDelegatePrice": 0,
                    "profitDelegateTimeInForce": "GTC",
                    "stopDelegateOrderType": "LIMIT",
                    "stopDelegatePrice": 0,
                    "stopDelegateTimeInForce": "GTC"
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
