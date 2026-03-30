---
title: 取消止盈止损
position_number: 8
type: post
description: /future/trade/v1/entrust/cancel-profit-stop
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

    | invalid_entrust | 订单ID有误 |

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
