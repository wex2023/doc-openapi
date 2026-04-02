---
title: 获取资金费率信息
position_number: 8
type: get
description: /future/user/v1/balance/funding-rate-list
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对（不传则查询所有交易对）
        ranges: 
    -
        name: direction
        type: string
        mandatory: false
        default: 'NEXT'
        description: 分页方向（PREV：上一页；NEXT：下一页）
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: 
        description: 记录 ID
        ranges: 
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: 每页条数
        ranges: 
    -
        name: startTime
        type: integer
        mandatory: false
        default: 
        description: 起始时间
        ranges: 
    -
        name: endTime
        type: integer
        mandatory: false
        default: 
        description: 结束时间
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
            "result": {
            "hasNext": false,       // 是否有下一页
            "hasPrev": false,       // 是否有上一页
            "items": [
            {
            "cast": 0,          // 资金费用
            "coin": "",         // 币种
            "createdTime": 0,   // 时间
            "id": 0,            // 记录ID
            "positionSide": "", // 持仓方向
            "symbol": ""        // 交易对
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
