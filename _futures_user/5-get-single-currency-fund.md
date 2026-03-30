---
title: Get User's Single Currency Fund Information
position_number: 5
type: get
description: /future/user/v1/balance/detail
parameters:
    -
        name: coin
        type: string
        mandatory: true
        default:
        description: Currency eg:btc
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getBalanceDetail() {

            }
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
              "error": {
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": {
                "availableBalance": 0,      //Available balance
                "coin": "",                 //Currency
                "isolatedMargin": 0,        //Frozen isolated margin
                "openOrderMarginFrozen": 0, //Frozen order
                "crossedMargin": 0,         //Crossed Margin
                "bonus": 0,                 //Bonus
                "coupon": 0,                //Coupon
                "walletBalance": 0          //Balance
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
