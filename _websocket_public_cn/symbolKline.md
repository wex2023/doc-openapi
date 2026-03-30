---
title: K线
position_number: 8
type:
description:

parameters:
    -
        name:
        type: string
        mandatory: false
        default:
        description:
        ranges:
content_markdown: |-
    **请求**

    &nbsp;

    格式: kline@\{symbol\},\{interval\}

    时间间隔: 1m, 3m, 5m, 15m, 30m, 1h, 2h, 4h, 6h, 8h, 12h, 1d, 3d, 1w, 1M

    示例: kline@btc\_usdt,5m

    频率: 1000ms

    &nbsp;
left_code_blocks:
    -
        code_block:
        title: 请求
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "kline",
                "event": "kline@btc_usdt,5m",
                "data": {
                    "s": "btc_usdt",       // 交易对
                    "t": 1656043200000,    // 时间
                    "i": "5m",             // 间隔
                    "o": "44000",          // 开盘价
                    "c": "50000",          // 收盘价
                    "h": "52000",          // 最高价
                    "l": "36000",          // 最低价
                    "q": "34.2",           // 成交量
                    "v": "230000"          // 成交额
                }
            }
        title: 响应
        language: json
---
