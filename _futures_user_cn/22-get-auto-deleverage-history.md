---
title: 查询自动减仓历史
position_number: 22
type: get
description: /future/user/v1/auto-deleverage/history
parameters:
    -
        name: id
        type: integer
        mandatory: false
        default: '1'
        description: 页码
        ranges: 
    -
        name: direction
        type: string
        mandatory: false
        default: 'NEXT'
        description: 方向
        ranges: NEXT;PREVIOUS
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
            "id": "2876543210987654321",           // ADL记录ID
            "symbol": "BTCUSDT",                   // 交易对
            "positionSide": "LONG",                // LONG 多头 / SHORT 空头
            "quantity": "0.028",                    // 被ADL强制减仓的数量（张）
            "price": "67234.50",                   // ADL执行时的成交价格
            "realizedProfit": "-87.60",            // 本次ADL产生的已实现盈亏
            "createdTime": 1735698765432,          // ADL发生时间戳（毫秒）
            "welfareAccount": false,               // 是否为体验金账户
            "uid": 10086,                          // 用户UID
            "accountId": 900123456789              // 账户ID
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
