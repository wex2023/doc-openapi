---
title: Batch Cancel Orders
position_number: 8
type: post
description: /future/trade/v1/order/cancel-batch
parameters:
    -
        name: orderIds
        type: string
        mandatory: true
        default:
        description: Order IDs (comma-separated)
        ranges:
    -
        name: clientOrderIds
        type: string
        mandatory: false
        default:
        description: Client order IDs (comma-separated)
        ranges:
content_markdown: >-
    #### Limit Flow Rules


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
