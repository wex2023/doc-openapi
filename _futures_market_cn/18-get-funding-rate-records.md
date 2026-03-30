---
title: 获取资金费率记录
position_number: 18
type: get
description: /future/market/v1/public/q/funding-rate-record
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对
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
        description: 限制条数
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
            "collectionInternal": 0, // 收费周期（秒）
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
