---
title: 获取指定交易对的聚合行情信息
position_number: 15
type: get
description: /future/market/v1/public/q/agg-ticker
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
        ranges: 

content_markdown: >-
    此方法不需要签名。
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
            "a": "",  // 24小时成交额
            "ap": "", // 卖一价
            "bp": "", // 买一价
            "c": "",  // 最新价
            "h": "",  // 24小时最高价
            "i": "",  // 指数价格
            "l": "",  // 24小时最低价
            "m": "",  // 标记价格
            "o": "",  // 24小时前第一笔成交价
            "r": "",  // 24小时价格涨跌幅
            "s": "",  // 交易对
            "t": 0,   // 时间
            "v": ""   // 24小时成交量
            },
            "returnCode": 0
            }
        title: Response
        language: json
---
