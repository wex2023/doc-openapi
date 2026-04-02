---
title: 获取用户阶梯费率
position_number: 11
type: get
description: /future/user/v1/user/step-rate
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
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
            "msgInfo": "success",
            "result": {
            "specialType": false,              // 是否为特殊账户
            "vipProType": true,                // 是否为专业费率
            "stepRateProName": "VIP_PRO_1",    // 专业费率等级名称
            "discountLevel": 2,                // 折扣等级
            "makerFee": "0.0015",              // 挂单手续费率
            "takerFee": "0.0025",              // 吃单手续费率
            "levelReturnDay": 30,              // 当前等级保留天数
            "totalTradeVolume": "1250000.50",  // 近29天+当天交易量
            "uBasedTotalTradeVolume": "850000.75",   // USDT本位合约交易量
            "coinBasedTotalTradeVolume": "400000.25",// 币本位合约交易量
            "walletBalance": "50000.00",       // 账户权益
            "notProfit": "1250.50",            // 持仓未实现盈亏
            "nextLvTradeVolume": "1500000.00", // 下一等级所需交易量
            "lackTradeVolume": "250000.50",    // 距离下一等级所需的交易量
            "nextLvWalletBalance": "75000.00", // 下一等级所需账户权益
            "lackWalletBalance": "25000.00",   // 距离下一等级所需的账户权益
            "nextLvMakerFee": "0.0010",        // 下一等级挂单手续费率
            "nextLvTakerFee": "0.0020"         // 下一等级吃单手续费率
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
