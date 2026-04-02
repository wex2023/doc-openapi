---
title: 获取用户单币种资金信息
position_number: 5
type: get
description: /future/user/v1/balance/detail
parameters:
    -
        name: coin
        type: string
        mandatory: true
        default: 
        description: 币种 eg:btc
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
            "availableBalance": 0,      // 可用余额
            "coin": "",                 // 币种
            "isolatedMargin": 0,        // 冻结逐仓保证金
            "openOrderMarginFrozen": 0, // 冻结委托保证金
            "crossedMargin": 0,         // 全仓保证金
            "bonus": 0,                 // 奖励金
            "coupon": 0,                // 抵扣券
            "walletBalance": 0          // 钱包余额
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
