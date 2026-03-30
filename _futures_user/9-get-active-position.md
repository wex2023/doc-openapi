---
title: Get active position information
position_number: 9
type: get
description: /future/user/v1/position
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pairs (queries position information for all trading pairs when not provided)
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getActivePosition() {

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
                "args": [],
                "code": "",
                "msg": ""
              },
              "msgInfo": "",
              "result": [
                {
                  "autoMargin": false,          // Whether to automatically call margin
                  "availableCloseSize": 0,      // Available quantity (Cont)
                  "breakPrice": 0,              // Blowout price
                  "calMarkPrice": 0,            // Calculated mark price
                  "closeOrderSize": 0,          // Quantity of open order (Cont)
                  "contractType": "",           // Contract Types: PERPETUAL, PREDICT
                  "entryPrice": 0,              // Average opening price
                  "floatingPL": 0,              // Unrealized profit or loss
                  "isolatedMargin": 0,          // Warehouse-by-warehouse margin
                  "leverage": 0,                // Leverage ratio
                  "openOrderMarginFrozen": 0,   // Occupation of deposit for opening order
                  "openOrderSize": 0,           // Opening warehouse orders occupied
                  "positionSide": "",           // Position direction
                  "positionSize": 0,            // Position quantity (Cont)
                  "positionType": "",           // Position type: CROSSED; ISOLATED
                  "profitId": 0,                // Take profit and stop loss id
                  "realizedProfit": 0,          // Realized profit and loss
                  "symbol": "",                 // Trading pair
                  "triggerPriceType": "",        // Trigger price type
                  "triggerProfitPrice": 0,      // Take profit trigger price
                  "triggerStopPrice": 0,        // Stop loss trigger price
                  "welfareAccount": true
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
