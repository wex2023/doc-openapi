---
title: 撤销订单
position_number: 7
type: post
description: /future/trade/v1/order/cancel
parameters:
    -
        name: orderId
        type: integer
        mandatory: true
        default:
        description: 订单 ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_params | 参数错误 订单不存在 |

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
              "result": "",
              "returnCode": 0
            }
        title: Response
        language: json
---
