---
title: 查询有成交的历史订单
position_number: 28
type: get
description: /future/trade/v1/order/trade-history
parameters:
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: "数量（最大为500）"
        ranges:
    -
        name: startTime
        type: integer
        mandatory: false
        default:
        description: "开始时间（默认查询90天前）"
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
        mandatory: true
        default:
        description: 交易对
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
              "result": [
                {
                  "symbol": "BTCUSDT",
                  "orderSide": "BUY",
                  "avgPrice": "67234.50",
                  "origQty": "0.012",
                  "executedQty": "0.012",
                  "updatedTime": 1735698765000
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
