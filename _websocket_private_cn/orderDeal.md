---
title: 订单成交
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
    **订阅格式：** trade

    &nbsp;

    当发生成交（订单成交）时触发此推送通知。
    包含成交详情，如成交 ID、订单 ID、价格、数量和 maker/taker 信息。
    可用于实时跟踪已完成的交易。
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["trade"],
                "listenKey": "512312356123123123"
            }
        title: 订阅
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "trade",
                "event": "trade",
                "data": {
                    "s": "btc_usdt",                // 交易对
                    "i": 6316559590087222000,       // 成交 ID
                    "t": 1655992403617,             // 成交时间（毫秒）
                    "oi": 6616559590087222666,      // 订单 ID
                    "p": "43000",                   // 价格
                    "q": "0.21",                    // 数量
                    "v": "9030",                    // 报价数量
                    "b": true,                      // 买方是否为 maker（true=买方为 maker）
                    "tm": 1                         // Taker/maker：1 = taker，2 = maker
                }
            }
        title: 推送
        language: json
---
