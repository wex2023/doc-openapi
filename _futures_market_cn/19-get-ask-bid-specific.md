---
title: 获取指定交易对的买卖盘行情信息
position_number: 19
type: get
description: /future/market/v1/public/q/ticker/book
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
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
            "ap": "", // 卖一价
            "aq": "", // 卖一量
            "bp": "", // 买一价
            "bq": "", // 买一量
            "s": "",  // 交易对
            "t": 0    // 时间
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
