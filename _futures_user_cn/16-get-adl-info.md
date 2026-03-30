---
title: 获取ADL信息
position_number: 16
type: get
description: /future/user/v1/position/adl
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对（不传时查询所有交易对的持仓信息）
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
            "result": [
            {
            "longQuantile": 0,   // 多头仓位ADL档位
            "shortQuantile": 0,  // 空头仓位ADL档位
            "symbol": ""         // 交易对
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
