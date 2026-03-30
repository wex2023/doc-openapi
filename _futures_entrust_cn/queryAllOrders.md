---
title: 查询全部委托
position_number: 30
type: get
description: /future/trade/v1/order-entrust/list
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
        type: long
        mandatory: false
        default:
        description: 开始时间
        ranges:
    -
        name: endTime
        type: long
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
    -
        name: type
        type: string
        mandatory: false
        default: ORDER
        description: "委托类型：ORDER（限价/市价委托）或 ENTRUST（计划委托）"
        ranges:
    -
        name: state
        type: string
        mandatory: false
        default:
        description: 订单状态
        ranges: NEW;PARTIALLY_FILLED;FILLED;CANCELED;REJECTED;PLACED;UNFINISHED;HISTORY
    -
        name: forceClose
        type: bool
        mandatory: false
        default: "false"
        description: 是否强平
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_size | size不正确 |

    | invalid_page | page参数设置不正确 |

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
                "page": 1,
                "ps": 10,
                "total": 99,
                "items": [
                  {
                    "id": "1876543210987654321",
                    "type": "ORDER",
                    "symbol": "BTCUSDT",
                    "orderType": "LIMIT",
                    "orderSide": "BUY",
                    "positionSide": "LONG",
                    "timeInForce": "GTC",
                    "closePosition": false,
                    "price": "67200.00",
                    "origQty": "0.015",
                    "avgPrice": "67234.50",
                    "executedQty": "0.015",
                    "marginFrozen": "50.42",
                    "leverage": 25,
                    "state": "FILLED",
                    "createdTime": 1735698000000,
                    "updatedTime": 1735698765000,
                    "positionType": "ISOLATED"
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
