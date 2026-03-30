---
title: 查询全仓维持保证金
position_number: 34
type: get
description: "/future/trade/v1/position/cross-margin/{symbol}"
parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    symbol 通过 URL 路径参数传递，例如：`/future/trade/v1/position/cross-margin/eth_usdt`


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
              "result": "result",
              "returnCode": 0
            }
        title: Response
        language: json
---
