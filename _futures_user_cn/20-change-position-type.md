---
title: 修改持仓模式
position_number: 20
type: post
description: /future/user/v1/position/change-type
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
        name: positionType
        type: string
        mandatory: true
        default: 
        description: 仓位模式
        ranges: CROSSED;ISOLATED

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
