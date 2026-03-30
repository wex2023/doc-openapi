---
title: 获取交易对最新成交信息
position_number: 8
type: get
description: /future/market/v1/public/q/deal
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 
    -
        name: num
        type: integer
        mandatory: false
        default: '50'
        description: 数量
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
            "result": [
            {
            "a": 0,  // 成交量
            "m": "", // 订单方向
            "p": 0,  // 价格
            "s": "", // 交易对
            "t": 0   // 时间
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
