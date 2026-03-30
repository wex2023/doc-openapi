---
title: 获取币种资产列表
position_number: 3
type: get
description: /v4/balances
parameters:
    -
        name: currencies
        type: string
        mandatory: false
        default:
        description: "币种列表，逗号分隔，例如：usdt,btc"
        ranges:
content_markdown: >-
    #### **限流规则**

    10次/秒/apikey
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
                  "mc": "string",
                  "ma": [
                    {}
                  ],
                  "result": {
                    "totalBtcAmount": 0,
                    "assets": [
                      {
                        "currency": "string",        // 币种
                        "currencyId": 0,             // 币种ID
                        "frozenAmount": 0,           // 冻结数量
                        "availableAmount": 0,        // 可用数量
                        "totalAmount": 0,            // 总数量
                        "convertBtcAmount": 0        // 折算BTC数量
                      }
                    ]
                  }
                }
        title: Response
        language: json
---
