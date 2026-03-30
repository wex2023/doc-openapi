---
title: 查询历史止盈止损委托
position_number: 24
type: get
description: /future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: "1"
        description: 页码
        ranges:
    -
        name: limit
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
        mandatory: false
        default:
        description: 交易对
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 翻页方向
        ranges: NEXT;PREVIOUS
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_direction | direction 不正确 |

    | invalid_limit | limit参数设置不正确 |

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
                    "profitId": "",
                    "symbol": "BTCUSDT",
                    "positionSide": "LONG",
                    "origQty": "0.020",
                    "leverage": 20,
                    "triggerPriceType": "MARK_PRICE",
                    "triggerProfitPrice": "68500.00",
                    "triggerStopPrice": "59500.00",
                    "entryPrice": "63250.80",
                    "positionSize": "0.020",
                    "isolatedMargin": "63.25",
                    "executedQty": "0.020",
                    "avgPrice": "68320.50",
                    "positionType": "ISOLATED",
                    "state": "TRIGGERED",
                    "createdTime": 1735689000000,
                    "updatedTime": 1735690123000,
                    "sourceType": "WEB",
                    "profitType": 0,
                    "mmrThreshold": null
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
