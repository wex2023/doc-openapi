---
title: 获取活跃持仓信息
position_number: 9
type: get
description: /future/user/v1/position
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default: 
        description: 交易对（不传时查询所有交易对的持仓信息）
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
            "error": { "args": [], "code": "", "msg": "" },
            "msgInfo": "",
            "result": [
            {
            "autoMargin": false,          // 是否自动追加保证金
            "availableCloseSize": 0,      // 可平仓数量（张）
            "breakPrice": 0,              // 强平价格
            "calMarkPrice": 0,            // 计算标记价格
            "closeOrderSize": 0,          // 已挂单数量（张）
            "contractType": "",           // 合约类型：PERPETUAL、PREDICT
            "entryPrice": 0,              // 开仓均价
            "floatingPL": 0,              // 未实现盈亏
            "isolatedMargin": 0,          // 仓位保证金（逐仓）
            "leverage": 0,                // 杠杆倍数
            "openOrderMarginFrozen": 0,   // 开仓委托冻结保证金
            "openOrderSize": 0,           // 开仓委托占用数量
            "positionSide": "",           // 仓位方向
            "positionSize": 0,            // 仓位数量（张）
            "positionType": "",           // 仓位类型：CROSSED；ISOLATED
            "profitId": 0,                // 止盈止损ID
            "realizedProfit": 0,          // 已实现盈亏
            "symbol": "",                 // 交易对
            "triggerPriceType": "",        // 触发价格类型
            "triggerProfitPrice": 0,      // 止盈触发价
            "triggerStopPrice": 0,        // 止损触发价
            "welfareAccount": true        // 是否为福利账户
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
