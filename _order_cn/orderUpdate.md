---
title: 更新订单（限价）
position_number: 10
type: put
description: /v4/order/{orderId}
parameters:
    -
        name: orderId
        type: number
        mandatory: true
        default:
        description: 订单ID
        ranges:
    -
        name: price
        type: number
        mandatory: true
        default:
        description: 价格
        ranges:
    -
        name: quantity
        type: number
        mandatory: true
        default:
        description: 数量
        ranges:
content_markdown: >-
    #### **限流规则**

    50次/秒/每apikey
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
                  "rc": 0,
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "orderId": "6216559590087220004",
                    "modifyId": "407329711723834560"
                  }
                }
        title: Response
        language: json
---
