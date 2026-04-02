---
title: 收藏交易对
position_number: 17
type: post
description: /future/user/v1/user/collection/add
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 

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
            "result": true,
            "returnCode": 0
            }
        title: Response
        language: json
---
