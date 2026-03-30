---
title: 获取用户资金流水信息
position_number: 7
type: get
description: /future/user/v1/balance/bills
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对（不传则查询全部）
        ranges: 
    -
        name: direction
        type: string
        mandatory: false
        default: 'NEXT'
        description: "查询方向（PREV: 上一页；NEXT: 下一页）"
        ranges: PREV;NEXT
    -
        name: id
        type: integer
        mandatory: false
        default: 
        description: 记录ID
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
        description: 开始时间
        ranges: 
    -
        name: endTime
        type: integer
        mandatory: false
        default: 
        description: 结束时间
        ranges: 

content_markdown: >-
    #### **限流规则**\n\n\n    200次/秒/apikey
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
            "hasNext": false,           // 是否有下一页
            "hasPrev": false,           // 是否有上一页
            "items": [
            {
            "afterAmount": 0,       // 变动后的余额
            "amount": 0,            // 变动数量
            "coin": "",             // 币种
            "createdTime": 0,       // 时间戳
            "id": 0,                // 记录ID
            "side": "",             // ADD: 转入；SUB: 转出
            "symbol": "",           // 交易对
            "type": ""              // EXCHANGE: 转账；CLOSE_POSITION: 平仓盈亏；TAKE_OVER: 仓位接管；FUND: 资金费率；FEE: 手续费；ADL: 自动减仓；MERGE: 仓位合并
            }
            ]
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
