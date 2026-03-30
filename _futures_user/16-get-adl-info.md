---
title: Get ADL Information
position_number: 16
type: get
description: /future/user/v1/position/adl
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: Trading pair (if not provided, query positions for all trading pairs)
        ranges:
content_markdown: >-
    #### **Limit Flow Rules**


    200/s/apikey
left_code_blocks:
    -
        code_block: |-
            public void getAdlInfo() {

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
                  "longQuantile": 0,  //long position adl
                  "shortQuantile": 0, //Short position adl
                  "symbol": ""        //Trading pair
                }
              ],
              "returnCode": 0
            }
        title: Response
        language: json
---
