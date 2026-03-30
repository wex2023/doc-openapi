---
title: 获取交易对的持仓量
position_number: 22
type: get
description: /future/market/v1/public/contract/open-interest
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
        ranges: 

content_markdown: >-
    #### **限流规则**\n\n\n    1次/秒/IP\n\n\n    此方法不需要签名。
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
            "symbol": "",          // 交易对
            "openInterest": "",    // 持仓量
            "openInterestUsd": 0,  // 持仓价值
            "time": ""             // 时间
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
