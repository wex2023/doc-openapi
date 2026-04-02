---
title: 获取合约账户资产
position_number: 2
type: get
description: /future/user/v1/compat/balance/list
parameters:
    -
        name: queryAccountId
        type: string
        mandatory: false
        default: 
        description: 账户 ID
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
            "accountId": 500000000000,     // 账户ID
            "userId": 500000000000,        // 用户ID
            "coin": "usdt",                // 币种
            "underlyingType": 2,           // 币种标准，U本位
            "walletBalance": "2078.57264793",  // 钱包余额
            "openOrderMarginFrozen": "0",  // 委托单冻结
            "isolatedMargin": "0",         // 逐仓保证金
            "crossedMargin": "0",          // 全仓保证金
            "amount": "2078.57264793",     // 净资产余额
            "totalAmount": "2078.57264793",// 保证金余额
            "convertBtcAmount": "0.03638940", // 钱包余额折算BTC
            "convertUsdtAmount": "2078.5726", // 钱包余额折算USDT
            "profit": "0",                 // 已实现盈亏
            "notProfit": "0",              // 未实现盈亏
            "bonus": "0",                  // 奖励金
            "coupon": "0"                  // 抵扣券
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
