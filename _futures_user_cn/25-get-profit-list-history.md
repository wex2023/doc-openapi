---
title: 查询历史止盈止损委托
position_number: 25
type: get
description: /future/trade/v1/entrust/profit-list-history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: '1'
        description: 页码
        ranges: 
    -
        name: limit
        type: integer
        mandatory: false
        default: '10'
        description: 单页数量
        ranges: 
    -
        name: startTime
        type: integer
        mandatory: false
        default: 
        description: 开始时间（默认查询90天前）
        ranges: 
    -
        name: endTime
        type: integer
        mandatory: false
        default: 
        description: 结束时间
        ranges: 
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
        description: 方向
        ranges: NEXT;PREVIOUS

content_markdown: >-
    #### **限流规则**\n\n\n    200/s/apikey
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
            "hasNext": false,
            "hasPrev": false,
            "items": [
            {
            "profitId": ""  // 委托id（Long转string）
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
