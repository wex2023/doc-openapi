---
title: Get Contract Account Assets
position_number: 2
type: get
description: /future/user/v1/compat/balance/list
parameters:
    -
        name: queryAccountId
        type: string
        mandatory: false
        default:
        description: Account ID
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getContractAccountAssets() {

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
              "result": [
                {
                  "accountId": 500000000000,              // account id
                  "userId": 500000000000,                 // user id
                  "coin": "usdt",                         // Currency
                  "underlyingType": 2,                    // Coin standard, u standard
                  "walletBalance": "2078.57264793",       // Currency balance
                  "openOrderMarginFrozen": "0",           // Order frozen
                  "isolatedMargin": "0",                  // Margin freeze
                  "crossedMargin": "0",                   // Full margin freeze
                  "amount": "2078.57264793",              // Net asset balance
                  "totalAmount": "2078.57264793",         // Margin balance
                  "convertBtcAmount": "0.03638940",       // walletBalance conversion BTC
                  "convertUsdtAmount": "2078.5726",       // walletBalance conversion USDT
                  "profit": "0",                          // Profit and loss
                  "notProfit": "0",                       // Unrealized profit/loss
                  "bonus": "0",                           // Trial fee
                  "coupon": "0"                           // Deduction
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
