---
title: 获取爆仓预警信息
position_number: 21
type: get
description: /future/user/v1/position/break-list
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对（不传时查询所有交易对的爆仓预警信息）
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
            "result": [
            {
            "breakPrice": 0,        // 爆仓价格，0代表不爆仓
            "calMarkPrice": 0,      // 标记价格
            "contractType": "",     // 合约类型：PERPETUAL 永续合约；PREDICT 预测合约
            "entryPrice": 0,        // 开仓均价
            "isolatedMargin": 0,    // 逐仓保证金
            "leverage": 0,          // 杠杆倍数
            "positionSide": "",     // 持仓方向：LONG 多头；SHORT 空头
            "positionSize": 0,      // 持仓数量（张）
            "positionType": "",     // 仓位类型：CROSSED 全仓；ISOLATED 逐仓
            "symbol": ""            // 交易对
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
