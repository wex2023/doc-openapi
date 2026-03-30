---
title: 成交记录
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

    格式: trade@\{symbol\}

    示例: trade@btc\_usdt

    频率: 实时
left_code_blocks:
    -
        code_block:
        title: 请求
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade",
                "event": "trade@btc_usdt",
                "data": {
                    "s": "btc_usdt",              // 交易对
                    "i": 6316559590087222000,     // 交易ID
                    "t": 1655992403617,           // 成交时间
                    "oi": 6616559590087222666,    // 订单ID
                    "p": "43000",                 // 成交价格
                    "q": "0.21",                  // 成交数量
                    "v": "9030",                  // 计价数量
                    "b": true                     // 方向(buyerMaker)
                }
            }
        title: 响应
        language: json
---
