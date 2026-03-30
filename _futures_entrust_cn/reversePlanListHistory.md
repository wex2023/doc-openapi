---
title: 查询历史计划反手
position_number: 27
type: get
description: /future/trade/v1/entrust/reverse-plan-list-history
parameters:
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
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
content_markdown: >-
    **注意：** 该接口限制只能查询五分钟内的数据。


    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_position_type | Position type不正确 |

    | invalid_position_side | Position side不正确 |

    | invalid_profit_close_type | Position close type不正确 |

    | invalid_state | State 不正确 |

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
                    "entrustId": "",
                    "symbol": "",
                    "entrustType": "",
                    "orderSide": "",
                    "positionSide": "",
                    "timeInForce": "",
                    "closePosition": false,
                    "price": 0,
                    "origQty": 0,
                    "stopPrice": "",
                    "triggerPriceType": "",
                    "executedQty": 0,
                    "avgPrice": "",
                    "state": "",
                    "createdTime": "",
                    "updatedTime": "",
                    "clientOrderId": "",
                    "reverseOpenExecutedQty": 0,
                    "reverseOpenAvgPrice": 0,
                    "desc": ""
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
