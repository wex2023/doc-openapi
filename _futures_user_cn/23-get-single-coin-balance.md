---
title: 查询单币种资产
position_number: 23
type: get
description: /future/user/v1/compat/balance/{coin}
parameters:
    -
        name: coin
        type: string
        mandatory: true
        default: 
        description: 币种（路径参数）eg:usdt
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
            "rc": 0,
            "mc": "",
            "ma": "",
            "result": {
            "accountId": 900123456789,
            "userId": 10086,
            "coin": "USDT",
            "underlyingType": 2,
            "walletBalance": "15234.87654321",
            "openOrderMarginFrozen": "800.00000000",
            "isolatedMargin": "2150.50000000",
            "crossedMargin": "4300.00000000",
            "amount": "8434.37654321",
            "totalAmount": "12734.87654321",
            "convertBtcAmount": "0.22681500",
            "convertUsdtAmount": "15234.88",
            "profit": "1250.45",
            "notProfit": "-500.00",
            "bonus": "1000.00000000",
            "coupon": "300.00000000",
            "depositCoupon": "5000.00000000",
            "marginBalance": "13234.87654321",
            "openOrderFeeFrozen": "15.88"
            }
            }
        title: Response
        language: json
---
