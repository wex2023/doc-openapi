---
title: 取消触发订单
position_number: 2
type: post
description: /future/trade/v1/entrust/cancel-plan
parameters:
    -
        name: entrustId
        type: string
        mandatory: true
        default:
        description: 计划委托单 ID
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey


    #### 错误码


    | 错误码 | 描述 |

    | --- | --- |

    | invalid_params | 提交的参数有误或为空 |

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
              "result": {},
              "returnCode": 0
            }
        title: Response
        language: json
---
