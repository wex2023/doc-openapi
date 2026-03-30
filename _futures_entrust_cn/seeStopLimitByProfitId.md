---
title: 根据ProfitId查看止盈止损
position_number: 11
type: get
description: /future/trade/v1/entrust/profit-detail
parameters:
    -
        name: profitId
        type: integer
        mandatory: true
        default:
        description: 止盈止损订单ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_profit_id | Profit ID 不存在 |

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
                "triggerStopPrice": 0
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
