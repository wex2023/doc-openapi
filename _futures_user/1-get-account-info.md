---
title: Get Account Related Information
position_number: 1
type: get
description: /future/user/v1/account/info
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
            public void getAccountInfo() {

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
                "accountId": 0,             // Account ID
                "allowOpenPosition": false, // Is it possible to open position
                "allowTrade": false,        // Is it possible to trade
                "allowTransfer": false,     // Is it possible to transfer
                "openTime": "",             // Opening time
                "state": 0,                 // User status
                "userId": 0                 // User ID
              },
              "returnCode": 0
            }
        title: Response
        language: json
---
