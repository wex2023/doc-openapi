---
title: Get Margin Call Information
position_number: 21
type: get
description: /future/user/v1/position/break-list
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair (if not passed, queries liquidation info of all trading pairs)
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getMarginCallInfo() {

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
                  "breakPrice": 0,        //Margin call price. 0 means no margin call
                  "calMarkPrice": 0,      //Mark price
                  "contractType": "",     //Futures type: PERPETUAL;PREDICT
                  "entryPrice": 0,        //Open position average price
                  "isolatedMargin": 0,    //Isolated Margin
                  "leverage": 0,          //Leverage
                  "positionSide": "",     //Position side:LONG;SHORT
                  "positionSize": 0,      //Position quantity (Cont)
                  "positionType": "",     //Position type:CROSSED;ISOLATED
                  "symbol": ""            //Symbol
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
