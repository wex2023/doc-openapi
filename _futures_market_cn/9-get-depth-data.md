---
title: 获取交易对深度数据
position_number: 9
type: get
description: /future/market/v1/public/q/depth
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:btc_usdt
        ranges: 
    -
        name: level
        type: integer
        mandatory: true
        default: 
        description: 档位（最小:1，最大:50）
        ranges: 1~50

content_markdown: >-
    #### **限流规则**\n\n\n    10次/秒/IP\n\n\n    此方法不需要签名。
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
            "a": [], // 卖单
            "b": [], // 买单
            "s": "", // 交易对
            "t": 0,  // 时间
            "u": 0   // 更新ID
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
