---
title: 撤销所有订单
position_number: 9
type: post
description: /future/trade/v1/order/cancel-all
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对（传入空字符串则撤销所有交易对的订单）
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
