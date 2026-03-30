---
title: 调整保证金
position_number: 13
type: post
description: /future/user/v1/position/margin
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 
    -
        name: margin
        type: number
        mandatory: false
        default: 
        description: 数量
        ranges: 
    -
        name: positionSide
        type: string
        mandatory: false
        default: 
        description: 持仓方向
        ranges: LONG;SHORT
    -
        name: type
        type: string
        mandatory: false
        default: 
        description: "调整方向（ADD: 增加逐仓保证金, SUB: 减少逐仓保证金）"
        ranges: ADD;SUB

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
