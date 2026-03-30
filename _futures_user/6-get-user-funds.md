---
title: Get User's Funds Information
position_number: 6
type: get
description: /future/user/v1/balance/list
parameters:
    -
        name:
        type:
        mandatory: false
        default:
        description:
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getBalanceList() {

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
                  "availableBalance": 0,      // Available balance
                  "coin": "",                 // Currency
                  "isolatedMargin": 0,        // Frozen isolated margin
                  "openOrderMarginFrozen": 0, // Frozen order margin
                  "crossedMargin": 0,         // Crossed margin
                  "bonus": 0,                 // Bonus
                  "coupon": 0,                // Coupon
                  "walletBalance": 0          // Wallet balance
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
