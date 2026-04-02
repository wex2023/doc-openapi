---
title: 修改自动追加保证金
position_number: 14
type: post
description: /future/user/v1/position/auto-margin
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
        name: autoMargin
        type: boolean
        mandatory: true
        default: 
        description: 是否自动追加保证金
        ranges: true;false

content_markdown: >-
    #### **限流规则**


    200次/秒/apikey
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
