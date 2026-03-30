---
title: 查询历史仓位
position_number: 33
type: get
description: /future/trade/v1/position/list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: "1"
        description: 页码
        ranges:
    -
        name: direction
        type: string
        mandatory: false
        default: NEXT
        description: 翻页方向
        ranges: NEXT;PREVIOUS
    -
        name: limit
        type: integer
        mandatory: false
        default: "10"
        description: 单页数量
        ranges:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对
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
        name: positionType
        type: integer
        mandatory: false
        default:
        description: "仓位模式（1全仓、2逐仓；不传查询全部）"
        ranges:
    -
        name: isFullClose
        type: integer
        mandatory: false
        default:
        description: "平仓方式（0部分平仓、1全部平仓；不传全部）"
        ranges:
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
                    "id": "1987654321098765432",
                    "positionSide": "LONG",
                    "contractType": "PERPETUAL",
                    "symbol": "BTCUSDT",
                    "positionType": 2,
                    "closeProfit": "127.83",
                    "closePositionSize": "0.050",
                    "closeOpenPrice": "63250.80",
                    "closePrice": "65808.60",
                    "maxPositionSize": "0.080",
                    "openTime": 1735608000000,
                    "closeTime": 1735699200000,
                    "startLeverage": 25,
                    "endLeverage": 25,
                    "working": false,
                    "force": false,
                    "forceMarkPrice": null,
                    "totalFee": "18.92",
                    "totalFundFee": "3.41",
                    "welfareAccount": false
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
