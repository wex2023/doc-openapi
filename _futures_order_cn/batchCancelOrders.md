---
title: 批量撤销订单
position_number: 8
type: post
description: /future/trade/v1/order/cancel-batch
parameters:
    -
        name: orderIds
        type: string
        mandatory: true
        default:
        description: 订单 ID（逗号分隔）
        ranges:
    -
        name: clientOrderIds
        type: string
        mandatory: false
        default:
        description: 客户端订单 ID（逗号分隔）
        ranges:
content_markdown: >-
    #### 限流规则


    200/s/apikey

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
