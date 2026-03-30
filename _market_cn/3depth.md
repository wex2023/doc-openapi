---
title: 获取深度数据
position_number: 4
type: get
description: /v4/public/depth
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对 例如：btc_usdt
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '100'
        description: 最小查询数量为 100
        ranges: 1~500
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
                  "mc": "SUCCESS",
                  "ma": [],
                  "result": {
                    "timestamp": 1662445330524,          //时间戳
                    "lastUpdateId": 137333589606963580,  //最后更新记录
                    "bids": [                            //买盘 [价位,挂单量]
                      [
                        "200.0000",
                        "0.996000"
                      ],
                      [
                        "100.0000",
                        "0.001000"
                      ],
                      [
                        "20.0000",
                        "10.000000"
                      ]
                    ],
                    "asks": []                          //卖盘 [价位,挂单量]
                  }
                }
        title: Response
        language: json
---
