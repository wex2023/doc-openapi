---
title: 查看单个交易对的杠杆分层
position_number: 5
type: get
description: /future/market/v1/public/leverage/bracket/detail
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
            "leverageBrackets": [
            {
            "bracket": 0,            // 层级
            "maintMarginRate": 0,    // 维持保证金率
            "maxLeverage": 0,        // 最大杠杆
            "maxNominalValue": 0,    // 最大名义价值
            "maxStartMarginRate": 0, // 最大初始保证金率
            "minLeverage": 0,        // 最小杠杆
            "startMarginRate": 0,    // 初始保证金率
            "symbol": ""             // 交易对
            }
            ],
            "symbol": ""
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
