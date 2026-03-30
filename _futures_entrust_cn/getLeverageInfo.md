---
title: 获取杠杆信息
position_number: 32
type: get
description: /future/trade/v1/position/leverage/list
parameters:
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
              "result": {
                "hasNext": false,
                "hasPrev": false,
                "items": [
                  {
                    "symbol": "BTCUSDT",
                    "accountId": "",
                    "positionType": "ISOLATED",
                    "positionSide": "LONG",
                    "contractType": "PERPETUAL",
                    "leverage": 25
                  }
                ]
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
