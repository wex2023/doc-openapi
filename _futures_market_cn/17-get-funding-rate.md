---
title: 获取资金费率信息
position_number: 17
type: get
description: /future/market/v1/public/q/funding-rate
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
        ranges: 

content_markdown: >-
    #### **限流规则**


    1次/秒/IP


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
            "hasNext": false, // 是否有下一页
            "hasPrev": false, // 是否有上一页
            "items": [
            {
            "collectionInternal": 0, // 结算周期（小时）
            "createdTime": 0,        // 时间
            "fundingRate": 0,        // 最新资金费率
            "id": 0,                 // id
            "symbol": ""             // 交易对
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
