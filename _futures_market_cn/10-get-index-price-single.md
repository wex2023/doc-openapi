---
title: 获取单个交易对的指数价格
position_number: 10
type: get
description: /future/market/v1/public/q/symbol-index-price
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 

content_markdown: >-
    此方法不需要签名。
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
            "result": {
            "p": 0,  // 价格
            "s": "", // 交易对
            "t": 0   // 时间
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
