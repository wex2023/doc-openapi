---
title: 余额变动
position_number: 5
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
    **订阅格式：** balance

    &nbsp;

    当用户账户余额发生变化时触发此推送通知。
    支持 **SPOT** 和 **LEVER** 两种业务类型。
    可用于实时跟踪交易、充值、提现或转账后的余额变化。
left_code_blocks:
    -
        code_block: |-
            {
                "method": "subscribe",
                "params": ["balance"],
                "listenKey": "512312356123123123"
            }
        title: 订阅
        language: json
right_code_blocks:
    -
        code_block: |-
            {
                "topic": "balance",
                "event": "balance",
                "data": {
                    "a": "123",           // 账户 ID
                    "t": 1656043204763,   // 事件时间（毫秒）
                    "c": "btc",           // 币种
                    "b": "123",           // 现货总余额
                    "f": "11",            // 冻结金额
                    "z": "SPOT",          // 业务类型 [SPOT, LEVER]
                    "s": "btc_usdt"       // 交易对
                }
            }
        title: 推送
        language: json
---
