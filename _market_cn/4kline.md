---
title: 获取 K 线数据
position_number: 5
type: get
description: /v4/public/kline
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default:
        description: 交易对 例如：btc_usdt
        ranges:
    -
        name: interval
        type: string
        mandatory: true
        default:
        description: |-
            K 线类型，
            例如：1m
        ranges: '[1m;3m;5m;15m;30m;1h;2h;4h;6h;8h;12h;1d;3d;1w;1M]'
    -
        name: startTime
        type: number
        mandatory: false
        default:
        description: 开始时间戳
        ranges:
    -
        name: endTime
        type: number
        mandatory: false
        default:
        description: 结束时间戳
        ranges:
    -
        name: limit
        type: number
        mandatory: false
        default: '100'
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
                      "t": 1662601014832,   //开盘时间
                      "o": "30000",         //开盘价
                      "c": "32000",         //收盘价
                      "h": "35000",         //最高价
                      "l": "25000",         //最低价
                      "q": "512",           //成交量
                      "v": "15360000"       //成交额
                    }
                  ]
                }
        title: Response
        language: json
---
