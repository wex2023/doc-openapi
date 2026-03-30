---
title: 推送消息格式
position_number: 4
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
content_markdown:
left_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade",             //频道名称
                "event": "trade@btc_usdt",    //事件标识符（含交易对）
                "data": { }                   //数据载荷
            }
        title: 格式
        language: javascript
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade",
                "event": "trade@btc_usdt",
                "data": {
                    "s": "btc_usdt",
                    "i": 6316559590087222000,
                    "t": 1655992403617,
                    "oi": 6616559590087222666,
                    "p": "43000",
                    "q": "0.21",
                    "v": "9030",
                    "b": true
                }
            }
        title: 示例 - 成交记录（实时推送）
        language: json
---
