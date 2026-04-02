---
title: 获取持仓信息
position_number: 10
type: get
description: /future/user/v1/position/list
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对（不传时查询所有交易对的持仓信息）
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
            "result": [
            {
            "autoMargin": false,          // 是否自动追加保证金
            "availableCloseSize": 0,      // 可平仓数量（张）
            "closeOrderSize": 0,          // 挂单数量（张）
            "entryPrice": 0,              // 开仓均价
            "isolatedMargin": 0,          // 逐仓保证金
            "leverage": 0,                // 杠杆倍数
            "openOrderMarginFrozen": 0,   // 占用开仓保证金
            "positionSide": "",           // 持仓方向
            "positionSize": 0,            // 持仓数量（张）
            "positionType": "",           // 仓位类型
            "realizedProfit": 0,          // 已实现盈亏
            "symbol": ""                  // 交易对
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
