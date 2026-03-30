---
title: 获取账户相关信息
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
    #### **限流规则**\n\n\n    200次/秒/apikey
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
            "accountId": 0,             // 账户ID
            "allowOpenPosition": false, // 是否允许开仓
            "allowTrade": false,        // 是否允许交易
            "allowTransfer": false,     // 是否允许划转
            "openTime": "",             // 开户时间
            "state": 0,                 // 用户状态
            "userId": 0                 // 用户ID
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
