---
title: 取消所有止盈止损
position_number: 9
type: post
description: /future/trade/v1/entrust/cancel-all-profit-stop
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: "交易对，例如 btc_usdt"
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_symbol | 交易对不存在 |

    | fail | 内部异常 |

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
              "result": true,
              "returnCode": 0
            }
        title: Response
        language: json
---
