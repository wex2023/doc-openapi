---
title: 调整杠杆
position_number: 12
type: post
description: /future/user/v1/position/adjust-leverage
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 
    -
        name: positionSide
        type: string
        mandatory: true
        default: 
        description: 持仓方向
        ranges: LONG;SHORT
    -
        name: leverage
        type: integer
        mandatory: true
        default: 
        description: 杠杆倍数
        ranges: 

content_markdown: >-
    #### **限流规则**\n\n\n    200次/秒/apikey
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
            "error": { "code": "", "msg": "" },
            "msgInfo": "",
            "result": {},
            "returnCode": 0
            }
        title: Response
        language: json
---
