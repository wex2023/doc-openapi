---
title: 查询最近成交列表
position_number: 6
type: get
description: /v4/public/trade/recent
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '200'
        description:
        ranges: 1~1000
content_markdown: >-
    #### **限流规则**

    10次/秒/IP

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
                  "result": [
                    {
                      "i": 0,           //ID
                      "t": 0,           //成交时间
                      "p": "string",    //成交价
                      "q": "string",    //成交量
                      "v": "string",    //成交额
                      "b": true         //是否是buyerMaker
                    }
                  ]
                }
        title: Response
        language: json
---
