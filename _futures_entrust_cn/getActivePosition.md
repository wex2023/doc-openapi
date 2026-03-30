---
title: 获取当前持仓信息
position_number: 31
type: get
description: /future/trade/v1/position/list/active
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
        ranges:
    -
        name: isDelivery
        type: bool
        mandatory: false
        default: "false"
        description: 是否查询交割
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
                  "positionType": "ISOLATED",
                  "positionSide": "LONG",
                  "contractType": "PERPETUAL",
                  "positionSize": "0.032",
                  "closeOrderSize": "0.008",
                  "availableCloseSize": "0.024",
                  "entryPrice": "66543.21",
                  "openOrderSize": "0.010",
                  "isolatedMargin": "106.47",
                  "openOrderMarginFrozen": "33.27",
                  "realizedProfit": "87.65",
                  "autoMargin": false,
                  "leverage": 25,
                  "contractSize": "0.001",
                  "markPrice": "67234.80",
                  "updatedTime": "1735701234567",
                  "welfareExpirationTime": 1767225599000,
                  "mmrProfitId": null,
                  "mmrThreshold": null
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
