---
title: 行情
position_number: 11
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

    格式: ticker@\{symbol\}

    示例: ticker@btc\_usdt

    频率: 1000ms
left_code_blocks:
    -
        code_block:
        title: 请求
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "ticker",
                "event": "ticker@btc_usdt",
                "data": {
                    "s": "btc_usdt",      // 交易对
                    "t": 1657586700119,   // 最后成交时间
                    "cv": "-200",         // 24小时价格变化
                    "cr": "-0.02",        // 24小时价格变化(百分比)
                    "o": "30000",         // 开盘价
                    "c": "39000",         // 收盘价
                    "h": "38000",         // 最高价
                    "l": "40000",         // 最低价
                    "q": "4",             // 成交量
                    "v": "150000"         // 成交额
                }
            }
        title: 响应
        language: json
---
