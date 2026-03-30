---
title: 查看成交明细
position_number: 12
type: get
description: /future/trade/v1/order/trade-list
parameters:
    -
        name: orderId
        type: integer
        mandatory: false
        default:
        description: 订单 ID
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
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
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_page | 页面需为正整数 |

    | invalid_size | size 最大值为 100 |

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
                    "fee": 0,
                    "feeCoin": "",
                    "orderId": 0,
                    "execId": 0,
                    "price": 0,
                    "quantity": 0,
                    "symbol": "",
                    "timestamp": 0,
                    "takerMaker": "TAKER"
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
