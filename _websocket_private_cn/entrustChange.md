---
title: 委托变动
position_number: 6
display: 0
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
    **订阅格式：** trigger

    &nbsp;

    当**触发/委托订单**发生变化时触发此推送通知。
    可用于跟踪触发订单的创建、更新和状态变化。
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["trigger"],
                "listenKey": "512312356123123123"
            }
        title: 订阅
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trigger",
                "event": "trigger",
                "data": {
                    "s": "btc_usdt",                // 交易对
                    "t": 1656043204763,             // 事件时间（毫秒）
                    "i": "6216559590087220004",     // 触发订单 ID
                    "st": "NEW"                     // 状态（如 NEW、FILLED、CANCELED）
                }
            }
        title: 推送
        language: json
---
