---
title: 订单变动
position_number: 7
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
    **订阅格式：** order

    &nbsp;

    当**订单状态**发生变化时触发此推送通知。

    可能的订单状态（st）：

    - NEW - 新订单创建

    - PARTIALLY\_FILLED - 部分成交

    - FILLED - 完全成交

    - CANCELED - 订单取消

    - REJECTED - 订单拒绝

    - EXPIRED - 订单过期
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["order"],
                "listenKey": "512312356123123123"
            }
        title: 订阅
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "order",
                "event": "order",
                "data": {
                    "s": "btc_usdt",                // 交易对
                    "bc": "btc",                    // 基础币种
                    "qc": "usdt",                   // 报价币种
                    "t": 1656043204763,             // 发生时间（毫秒）
                    "ct": 1656043204663,            // 创建时间（毫秒）
                    "i": "6216559590087220004",     // 订单 ID
                    "ci": "test123",                // 客户订单 ID
                    "st": "PARTIALLY_FILLED",       // 状态 NEW/PARTIALLY_FILLED/FILLED/CANCELED/REJECTED/EXPIRED
                    "sd": "BUY",                    // 方向 BUY/SELL
                    "tp": "LIMIT",                  // 类型 LIMIT/MARKET
                    "oq": "4",                      // 原始数量
                    "oqq": 48000,                   // 原始报价数量
                    "eq": "2",                      // 已成交数量
                    "lq": "2",                      // 剩余数量
                    "p": "4000",                    // 价格
                    "ap": "30000",                  // 平均价格
                    "f": "0.002"                    // 手续费
                }
            }
        title: 推送
        language: json
---
