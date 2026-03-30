---
title: 获取交易对K线信息
position_number: 14
type: get
description: /future/market/v1/public/q/kline
parameters:
    -
        name: symbol
        type: string
        mandatory: true
        default: 
        description: 交易对 eg:eth_usdt
        ranges: 
    -
        name: interval
        type: string
        mandatory: true
        default: 
        description: 时间间隔
        ranges: 1m;5m;15m;30m;1h;4h;1d;1w
    -
        name: startTime
        type: integer
        mandatory: false
        default: 
        description: 开始时间
        ranges: 
    -
        name: endTime
        type: integer
        mandatory: false
        default: 
        description: 结束时间
        ranges: 
    -
        name: limit
        type: integer
        mandatory: false
        default: 
        description: 限制数量
        ranges: 1~1500

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
            "result": [
            {
            "a": 0,  // 成交量
            "c": 0,  // 收盘价
            "h": 0,  // 最高价
            "l": 0,  // 最低价
            "o": 0,  // 开盘价
            "s": "", // 交易对
            "t": 0,  // 时间
            "v": 0   // 成交额
            }
            ],
            "returnCode": 0
            }
        title: Response
        language: json
---
