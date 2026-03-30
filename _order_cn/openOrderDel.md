---
title: 取消当前挂单
position_number: 8
type: delete
split: -------------------------------------
description: /v4/open-order
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对，不填则表示全部
        ranges:
    -
        name: bizType
        type: string
        mandatory: true
        default:
        description: "业务类型 SPOT, LEVER"
        ranges:
    -
        name: side
        type: string
        mandatory: false
        default:
        description: "订单方向 BUY, SELL"
        ranges:
content_markdown: >-
    #### **限频规则**

    10次/秒/每apikey
    <br>
    注意：参数需以 JSON 格式放置于请求体中。
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
                  "result": {}
                }
        title: Response
        language: json
---
