---
title: 获取交易对风险基金余额
position_number: 21
type: get
description: /future/market/v1/public/contract/risk-balance
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
        ranges: 
    -
        name: direction
        type: string
        mandatory: false
        default: 'NEXT'
        description: 方向（PREV：上一页；NEXT：下一页）
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: 
        description: id
        ranges: 
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: 限制数量
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
            "hasNext": false, // 是否有下一页
            "hasPrev": false, // 是否有上一页
            "items": [
            {
            "amount": 0,      // 余额
            "coin": "",       // 币种
            "createdTime": 0, // 时间
            "id": 0           // id
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
