---
title: 全量行情
position_number: 8
type: get
description: /v4/public/ticker
parameters:
    -
        name: symbol
        type: string
        mandatory: false
        default:
        description: 交易对 例如：btc_usdt
        ranges:
    -
        name: symbols
        type: array
        mandatory: false
        default:
        description: '交易对集合，优先级高于symbol。例如：btc_usdt,eth_usdt'
        ranges:
    -
        name: tags
        type: string
        mandatory: false
        default:
        description: '标签集合，逗号分隔，目前仅支持 spot'
        ranges:
content_markdown: >-
    #### **限流规则**


    1\.单一交易对：10次/秒/IP


    2\.多个交易对：10次/秒/IP


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
                "result": [
                      {
                        "s": "btc_usdt",        //交易对
                        "t": 1662444879425,     //更新时间
                        "cv": "0.00",           //价格变动
                        "cr": "0.0000",         //价格变动百分比
                        "o": "200.00",          //最早一笔
                        "l": "200.00",          //最低
                        "h": "200.00",          //最高
                        "c": "200.00",          //最后一笔
                        "q": "0.002",           //成交量
                        "v": "0.40",            //成交额
                        "ap": null,             //卖一价
                        "aq": null,             //卖一量
                        "bp": null,             //买一价
                        "bq": null              //买一量
                        }
                    ]
            }
        title: Response
        language: json
---
